---
title: Запрос сведений о простых правах
description: Запрос сведений о простых правах
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows Media Format SDK, запрос простых прав
- Пакет SDK для Windows Media Format, простые запросы прав
- Управление цифровыми правами (DRM), запрос простых прав
- DRM (Управление цифровыми правами), запрос простых прав
- Управление цифровыми правами (DRM), простые запросы прав
- DRM (Управление цифровыми правами), запросы простых прав
- Расширенные API клиента DRM, запрос простых прав
- Расширенные API клиента, запросы простых прав
- Расширенные API клиента DRM, запросы простых прав
- Расширенные API клиента, запросы простых прав
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410964"
---
# <a name="querying-for-simple-rights-information"></a><span data-ttu-id="178ce-113">Запрос сведений о простых правах</span><span class="sxs-lookup"><span data-stu-id="178ce-113">Querying for Simple Rights Information</span></span>

<span data-ttu-id="178ce-114">Расширенные API клиента DRM Windows Media позволяют быстро получить сведения о том, можно ли получить доступ к защищенному содержимому для различных действий.</span><span class="sxs-lookup"><span data-stu-id="178ce-114">The Windows Media DRM Client Extended APIs enable you to quickly get simple information about whether protected content can be accessed for various actions.</span></span>

<span data-ttu-id="178ce-115">Метод [**ивмдрмлиценсекуери:: куеряктионалловед**](iwmdrmlicensequery-queryactionallowed.md) можно использовать, чтобы быстро определить, разрешено ли действие лицензией в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="178ce-115">The [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method can be used to determine quickly whether an action is permitted by a license in the local license store.</span></span> <span data-ttu-id="178ce-116">**Куеряктионалловед** оптимизирована так, чтобы выполняться гораздо быстрее, чем запросы на аналогичную информацию, используя объекты пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="178ce-116">**QueryActionAllowed** has been optimized to be much faster than queries for similar information using the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="178ce-117">Однако этот тип запроса объединяет лицензии в локальном хранилище лицензий и должен использоваться только для простых функций, например может потребоваться для элементов пользовательского интерфейса, например для отображения индикатора разрешений.</span><span class="sxs-lookup"><span data-stu-id="178ce-117">However, this type of query aggregates the licenses in the local license store and should be used only for simple features, such as might be needed for user interface elements, for example displaying a permission indicator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="178ce-118">См. также</span><span class="sxs-lookup"><span data-stu-id="178ce-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="178ce-119">**Получение сведений из лицензий в локальном хранилище лицензий**</span><span class="sxs-lookup"><span data-stu-id="178ce-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




