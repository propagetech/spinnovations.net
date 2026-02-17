You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "SP Innovations Technologies LLP | About Us",
      "first_heading": "About Us"
    }
  },
  {
    "path": "bank-auditing-reconciliation-system.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Bank Auditing and Reconciliation System",
      "first_heading": "Bank Auditing and Reconciliation System"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Contact Us",
      "first_heading": "Contact Us"
    }
  },
  {
    "path": "core-banking-software.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Core Banking Software",
      "first_heading": "Core Banking Software"
    }
  },
  {
    "path": "css/371e5c239daf91675528f453032eaab0.css",
    "context": {
      "path": "css/371e5c239daf91675528f453032eaab0.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "development-testing-web-application.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Development, Maintaining and Testing Web Application",
      "first_heading": "Development, Maintaining and Testing Web Application"
    }
  },
  {
    "path": "e-hospital.html",
    "context": {
      "title": "SP Innovations Technologies LLP | E- Hospital",
      "first_heading": "E- Hospital \u2013 Hospital Management System (HMS)"
    }
  },
  {
    "path": "enterprise-mobility-solutions.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Enterprise Mobility Solutions",
      "first_heading": "Enterprise Mobility Solutions (B2B) & (B2C)"
    }
  },
  {
    "path": "erp.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Enterprise Resource Planning",
      "first_heading": "Enterprise Resource Planning"
    }
  },
  {
    "path": "facial-recognition-solutions.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Attendance by Facial Recognition",
      "first_heading": "Attendance by Facial Recognition"
    }
  },
  {
    "path": "imgs/0017d849a1a84cd6428a217d05d512b6.webp",
    "context": {
      "refs": [
        {
          "alt": "OPERATIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/004e2d29e6ca646f93bf523f425145b1.webp",
    "context": {
      "refs": [
        {
          "alt": "sf",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/047c2fd937ff6d89974c56cc084704d7.webp",
    "context": {
      "refs": [
        {
          "alt": "Manufacturing sectors",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0957db9a471d1b0f8b9cc71a63bd5cd5.webp",
    "context": {
      "refs": [
        {
          "alt": "partner1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0dc4de3bdbcfb9ed2c9e23918824de5e.webp",
    "context": {
      "refs": [
        {
          "alt": "sf",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12d6478b2bd41d69f04e9861d17022c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12ecc76f14fec28631d4176556de203c.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/183abc4a9017db59e6f79ec9ffc25b47.webp",
    "context": {
      "refs": [
        {
          "alt": "Bank Auditing System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a568adb74a0e3b8d9e89e02ecd7022d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22305a5590f319b22dafe0b489837107.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/263a219e3789f4e72b83b5c2c8b8cc01.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR STRENGTH",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2dafacc1a0a04b843f2a92670394b711.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fd02c901a3c2adb557609b31691ac51.webp",
    "context": {
      "refs": [
        {
          "alt": "Attendance by Facial Recognition",
          "title": ""
        },
        {
          "alt": "Benefits",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31ff9e052cf4ceee42d56fa6cc4cfdfd.webp",
    "context": {
      "refs": [
        {
          "alt": "OTHERS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34a01269947ebfd0b45f8821a08e81d5.webp",
    "context": {
      "refs": [
        {
          "alt": "partner2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/354b2444c3162a1a9364f8df3990b218.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37eab80c672c8aa44b7f1fbd69eb7885.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3cf96fe5a714cfc03476cdefd1977543.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR STRENGTH",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3df8f63333f11114aba1f93e19e5fc3a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e1a6f9a879886dcd26119e78e4d91d5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4200e8fd0972d55bf94024aa505c4c06.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/448791ca23b894c308af28ed18e08e2c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5639800b89526df8b46959233031385c.webp",
    "context": {
      "refs": [
        {
          "alt": "ACCOUNTS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5eff356888d741700b1534fd9fd2243a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66f46c691e1ed56436f529d88e424dd5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6872415461a70e96a6fb017980c7c60c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6af8037db4c4878402c57ec198f21299.webp",
    "context": {
      "refs": [
        {
          "alt": "sf",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/715aae64449d072ea4c573558b947b4f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75be02661d4c74a4624800ae9e1c963b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bd0ae5c7e8fee8f56e7bf0975d3181d.webp",
    "context": {
      "refs": [
        {
          "alt": "Padmanabha Pandeshwar",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/863a5151cf0a03dc64a53338c7e17ddc.webp",
    "context": {
      "refs": [
        {
          "alt": "shutterstock",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86b6f41ae4fd255b792cf9f68ad03b3d.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8768af85ee423538c5550d23d1144f04.webp",
    "context": {
      "refs": [
        {
          "alt": "Features",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88214152e6e4f9692a9eb4e121e3ecdf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c93520e409ae9940e9897c468c23a3c.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92ebb7eb117435f674ec37fb4c4d59dd.webp",
    "context": {
      "refs": [
        {
          "alt": "sf",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/95b08824e17567477b6c051d4023aeb2.webp",
    "context": {
      "refs": [
        {
          "alt": "ITI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/97d13ebbb9c5f70a8396e0a91c995c33.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9aa5726779820957a58a61ace43b8e76.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af159383b45fe101665a268ee2675ac2.webp",
    "context": {
      "refs": [
        {
          "alt": "HAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b10f1cc14eb109d58e509b1881d3d168.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b324d910af8754e11f69d99dc72e3889.webp",
    "context": {
      "refs": [
        {
          "alt": "Krishnan Subramanian",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b545fb6f00b974ddfec450623d8153a1.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc727389e319351183de439bcbaeb4d4.webp",
    "context": {
      "refs": [
        {
          "alt": "Development, Maintaining and Testing Web Application",
          "title": ""
        },
        {
          "alt": "Capabilities",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c3189104b3436986c71af154ff7c5ef4.webp",
    "context": {
      "refs": [
        {
          "alt": "SPI Payment Gateway",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7b2c4e84c8d9d26554f0681c76814a9.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd2778da3a6595b1c386ec13abbdcbcc.webp",
    "context": {
      "refs": [
        {
          "alt": "Features",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd4d5015184d4e8e3ddd9e021678bc3a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce2cd039203ac47e6bcd50e6eb388fac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfc0ac0b2501cc3aa49d87844c9f0f6f.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5052e623ad39bcf24e8f79acb8a9224.webp",
    "context": {
      "refs": [
        {
          "alt": "Sudheer",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5b96b0ca5437922d4882944ade5a554.webp",
    "context": {
      "refs": [
        {
          "alt": "Dr. Dhruva",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5d98df50796aad355181a1754bb7142.webp",
    "context": {
      "refs": [
        {
          "alt": "Core Banking Software",
          "title": ""
        },
        {
          "alt": "Benefits",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d720a74727250a3477ccdac1c8af853c.webp",
    "context": {
      "refs": [
        {
          "alt": "E- Hospital \u2013 Hospital Management System",
          "title": ""
        },
        {
          "alt": "Benefits",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da909bd3c47c3b232b9e6b0f0d0b7d7a.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcde949a66da0d4dfab47496a2b66afc.webp",
    "context": {
      "refs": [
        {
          "alt": "sf",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e217224eab51259b1e10ccc4d23d7248.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e31b3bf202a03676eac19c97cfb5a7fa.webp",
    "context": {
      "refs": [
        {
          "alt": "NPST",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e41b46ee52045369a0a468bbf48cada2.webp",
    "context": {
      "refs": [
        {
          "alt": "Educational Institutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8013ac1b9987a9f9e6eb296942e3beb.webp",
    "context": {
      "refs": [
        {
          "alt": "shutterstock",
          "title": ""
        },
        {
          "alt": "Enterprise Mobility Solutions (B2B) & (B2C)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8560f1eaa36b2a1dfa133f02da5149f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec23c5f7f038f660ee0d091d73add5b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee654265dca6fabef600d100e01574ae.webp",
    "context": {
      "refs": [
        {
          "alt": "Core Banking Solutions - CBS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eeca732d671e7a464f2501ec96c7c5cb.webp",
    "context": {
      "refs": [
        {
          "alt": "Bank Auditing and Reconciliation System",
          "title": ""
        },
        {
          "alt": "Banking Reconciliation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f18ac300bfb5655b22174073ddef005c.webp",
    "context": {
      "refs": [
        {
          "alt": "Digital Transformation for Insurance Companies",
          "title": ""
        },
        {
          "alt": "Features",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2ce4af58f9bb1a41edb6c011ed1e314.webp",
    "context": {
      "refs": [
        {
          "alt": "sf",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f30e21c2fac04d7d3a62b50e16eb40f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fef137cf4a95526179f12b356395d881.webp",
    "context": {
      "refs": [
        {
          "alt": "Enterprise Resource Planning",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Home",
      "first_heading": "Enterprise Resource Planning (ERP)"
    }
  },
  {
    "path": "insurance-companies-solutions.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Digital Transformation for Insurance Companies",
      "first_heading": "Digital Transformation for Insurance Companies"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "payment-gateway-services.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Payment Gateway Services",
      "first_heading": "Payment Gateway Services"
    }
  },
  {
    "path": "privacy-policy.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Home",
      "first_heading": "Privacy Policy"
    }
  },
  {
    "path": "service-recharge.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Service Recharge",
      "first_heading": "Service Recharge"
    }
  },
  {
    "path": "terms-and-conditions.html",
    "context": {
      "title": "SP Innovations Technologies LLP | Home",
      "first_heading": "Terms and Conditions"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.