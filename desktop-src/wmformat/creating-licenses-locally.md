---
title: Создание лицензий локально
description: Создание лицензий локально
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Пакет SDK для Windows Media Format, создание лицензий в локальной среде
- Пакет SDK для Windows Media Format, лицензии
- Управление цифровыми правами (DRM), создание лицензий в локальной среде
- DRM (Управление цифровыми правами), создание лицензий локально
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Расширенные API клиента DRM, создание лицензий в локальной среде
- Расширенные API клиента, создание лицензий локально
- лицензии, создание лицензий локально
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068593"
---
# <a name="creating-licenses-locally"></a><span data-ttu-id="abdbc-112">Создание лицензий локально</span><span class="sxs-lookup"><span data-stu-id="abdbc-112">Creating Licenses Locally</span></span>

<span data-ttu-id="abdbc-113">В определенных обстоятельствах, например при [импорте DRM](drm-import.md), можно создавать собственные лицензии.</span><span class="sxs-lookup"><span data-stu-id="abdbc-113">In certain circumstances, such as during [DRM Import](drm-import.md), you can create your own licenses.</span></span> <span data-ttu-id="abdbc-114">Лицензии DRM Windows Media могут быть написаны несколькими разными способами, но для создания собственной лицензии необходимо использовать двоичную схему Extensible Media Rights (КСМР).</span><span class="sxs-lookup"><span data-stu-id="abdbc-114">Windows Media DRM licenses can be written a few different ways, but to make your own license, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="abdbc-115">Дополнительные сведения см. в разделе [Создание лицензии КСМР](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="abdbc-115">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>

<span data-ttu-id="abdbc-116">При создании лицензии ее можно добавить в локальное хранилище лицензий, вызвав метод [**ивмдрмлиценсеманажемент:: сторелиценсе**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="abdbc-116">When you create a license, you can add it to the local license store by calling the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abdbc-117">См. также</span><span class="sxs-lookup"><span data-stu-id="abdbc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abdbc-118">**Получение лицензий**</span><span class="sxs-lookup"><span data-stu-id="abdbc-118">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="abdbc-119">**Создание лицензии КСМР**</span><span class="sxs-lookup"><span data-stu-id="abdbc-119">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> </dl>

 

 




