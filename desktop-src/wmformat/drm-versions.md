---
title: Версии DRM
description: Версии DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK, версии DRM
- Управление цифровыми правами (DRM), версии
- DRM (Управление цифровыми правами), версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986333"
---
# <a name="drm-versions"></a><span data-ttu-id="b9cd8-106">Версии DRM</span><span class="sxs-lookup"><span data-stu-id="b9cd8-106">DRM Versions</span></span>

<span data-ttu-id="b9cd8-107">Существует несколько версий системы управления цифровыми правами (DRM) Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="b9cd8-108">DRM версии 1 часто устанавливаются отдельно от других версий в этой документации, так как она реализована с использованием методик, отличных от более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="b9cd8-109">Второе поколение Windows Media DRM называется DRM версии 7, поскольку оно было представлено в составе пакета SDK Windows Media Format 7.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="b9cd8-110">Иногда она называется DRM версии 2.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="b9cd8-111">Более поздние версии Windows Media DRM, DRM версии 9 и нового Windows Media DRM 10, являются расширениями DRM версии 7 и используют одни и те же процедуры для реализации.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="b9cd8-112">Все версии Windows Media DRM используют одни и те же подпрограммы шифрования. различия между версиями применяют функции лицензирования.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="b9cd8-113">При создании защищенных файлов с помощью объектов пакета SDK Windows Media Format необходимо поддерживать как версии 1, так и самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="b9cd8-114">Файлы, защищенные DRM версии 1, отличаются от файлов, защищенных более поздними версиями, только в содержимом заголовка.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="b9cd8-115">Новые файлы, содержащие дополнительные сведения о заголовке, по-прежнему могут использоваться на клиентах, которые отображают только содержимое версии 1.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="b9cd8-116">Несмотря на то, что более поздние версии DRM предлагают более высокий уровень безопасности и дополнительные функции, существует множество игроков, использующих только версию 1.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="b9cd8-117">Дополнительные сведения о версиях DRM см. в документации по пакету SDK для диспетчера прав Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="b9cd8-118">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b9cd8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b9cd8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9cd8-120">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="b9cd8-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="b9cd8-121">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="b9cd8-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




