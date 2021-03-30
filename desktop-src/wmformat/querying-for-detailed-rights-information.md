---
title: Запрос подробных сведений о правах
description: Запрос подробных сведений о правах
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Пакет SDK Windows Media Format, запрос подробных прав
- Пакет SDK для Windows Media Format, подробные запросы прав
- Управление цифровыми правами (DRM), запрос подробных прав
- DRM (Управление цифровыми правами), запрос подробных прав
- Управление цифровыми правами (DRM), запросы подробных прав
- DRM (Управление цифровыми правами), запросы подробных прав
- Расширенные API клиента DRM, запрос подробных прав
- Расширенные API клиента, запрос подробных прав
- Расширенные API клиента DRM, запросы подробных прав
- Расширенные API клиента, запросы подробных прав
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258515"
---
# <a name="querying-for-detailed-rights-information"></a><span data-ttu-id="029ec-113">Запрос подробных сведений о правах</span><span class="sxs-lookup"><span data-stu-id="029ec-113">Querying for Detailed Rights Information</span></span>

<span data-ttu-id="029ec-114">С помощью метода [**ивмдрмлиценсекуери:: куерилиценсестате**](iwmdrmlicensequery-querylicensestate.md) можно получить подробные сведения о правах, предоставляемые лицензиями для идентификатора ключа.</span><span class="sxs-lookup"><span data-stu-id="029ec-114">By using the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method, you can obtain detailed information about the rights granted by licenses for a key ID.</span></span> <span data-ttu-id="029ec-115">Сведения, получаемые от этого метода, суммируются по всем лицензиям в локальном хранилище лицензий, которые применяются к указанному ИДЕНТИФИКАТОРу ключа.</span><span class="sxs-lookup"><span data-stu-id="029ec-115">The information that you get from this method is aggregated from all licenses in the local license store that apply to the specified key ID.</span></span>

<span data-ttu-id="029ec-116">**Куерилиценсестате** использует структуру [**\_ данных о \_ состоянии \_ лицензии DRM**](drmdrm-license-state-data.md) для отображения статистических сведений обо всех лицензиях для указанного идентификатора ключа.</span><span class="sxs-lookup"><span data-stu-id="029ec-116">**QueryLicenseState** uses the [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure to display aggregate information about all the licenses for the specified key ID.</span></span> <span data-ttu-id="029ec-117">Это использование отличается от других объектов в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="029ec-117">This usage is different than by other objects in the Windows Media Format SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="029ec-118">См. также</span><span class="sxs-lookup"><span data-stu-id="029ec-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="029ec-119">**Получение сведений из лицензий в локальном хранилище лицензий**</span><span class="sxs-lookup"><span data-stu-id="029ec-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




