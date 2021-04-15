---
title: Удаление лицензий
description: Удаление лицензий
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Пакет SDK для Windows Media Format, лицензии
- Пакет SDK для Windows Media Format, Удаление лицензий
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
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654239"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание лицензии КСМР**](building-an-xmr-license.md)
</dt> <dt>

[**Импорт DRM**](drm-import.md)
</dt> <dt>

[**Инструкции по программированию**](drm-programming-guide.md)
</dt> </dl>

 

 




