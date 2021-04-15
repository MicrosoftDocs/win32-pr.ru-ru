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
# <a name="license-deletion"></a><span data-ttu-id="d448c-114">Удаление лицензий</span><span class="sxs-lookup"><span data-stu-id="d448c-114">License Deletion</span></span>

<span data-ttu-id="d448c-115">Любые лицензии сторонних производителей, созданные локально, например с помощью импорта DRM, можно удалить, вызвав метод [**ивмдрмлиценсеманажемент::P роцесслиценседелетионмессаже**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d448c-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="d448c-116">Строка, передаваемая в этот метод, будет КСМР лицензией, которая выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d448c-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


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



<span data-ttu-id="d448c-117">Поле идентификатора конкретного пользователя (UID) не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d448c-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="d448c-118">Необязательные поля не должны включаться в ответ лицензии, если с ними не связано никаких данных.</span><span class="sxs-lookup"><span data-stu-id="d448c-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d448c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d448c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d448c-120">**Создание лицензии КСМР**</span><span class="sxs-lookup"><span data-stu-id="d448c-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="d448c-121">**Импорт DRM**</span><span class="sxs-lookup"><span data-stu-id="d448c-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="d448c-122">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="d448c-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




