---
title: Удаление лицензий
description: Удаление лицензий
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Пакет SDK для формата мультимедиа, лицензии
- Windows Пакет SDK для формата мультимедиа, Удаление лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), Удаление лицензий
- DRM (Управление цифровыми правами), Удаление лицензий
- Расширенные API клиента DRM, лицензии
- Расширенные API клиента, лицензии
- Расширенные API клиента DRM, Удаление лицензий
- Расширенные API клиента, Удаление лицензий
- лицензии, удаление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd1e20c0e98fd2129b807cf11f27f5975701d851d9301eda894ccb24015360a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808304"
---
# <a name="license-deletion"></a>Удаление лицензий

Любые лицензии сторонних производителей, созданные локально, например с помощью импорта DRM, можно удалить, вызвав метод [**ивмдрмлиценсеманажемент::P роцесслиценседелетионмессаже**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) . Строка, передаваемая в этот метод, будет КСМР лицензией, которая выглядит следующим образом:


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



Поле идентификатора конкретного пользователя (UID) не является обязательным. Необязательные поля не должны включаться в ответ лицензии, если с ними не связано никаких данных.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание лицензии КСМР**](building-an-xmr-license.md)
</dt> <dt>

[**Импорт DRM**](drm-import.md)
</dt> <dt>

[**Инструкции по программированию**](drm-programming-guide.md)
</dt> </dl>

 

 




