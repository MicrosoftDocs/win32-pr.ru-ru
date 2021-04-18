---
title: Функции клиента DRM Microsoft Windows Media
description: Функции клиента DRM Microsoft Windows Media
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, функции
- Управление цифровыми правами (DRM), функции
- DRM (Управление цифровыми правами), функции
- Расширенные API клиента DRM, функции
- Расширенные API клиента, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105700995"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="04b08-108">Функции клиента DRM Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="04b08-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="04b08-109">В состав расширенных API клиента DRM Microsoft Windows Media реализуются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="04b08-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="04b08-110">Функция</span><span class="sxs-lookup"><span data-stu-id="04b08-110">Function</span></span>                                                             | <span data-ttu-id="04b08-111">Описание</span><span class="sxs-lookup"><span data-stu-id="04b08-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04b08-112">**вмдрмкреатепровидер**</span><span class="sxs-lookup"><span data-stu-id="04b08-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="04b08-113">Создает фабрику класса, которая может создавать другие объекты DRM.</span><span class="sxs-lookup"><span data-stu-id="04b08-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="04b08-114">Эта функция не требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, которые не поддерживают защищенные функции DRM.</span><span class="sxs-lookup"><span data-stu-id="04b08-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="04b08-115">**вмдрмкреатепротектедпровидер**</span><span class="sxs-lookup"><span data-stu-id="04b08-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="04b08-116">Создает фабрику класса, которая может создавать другие объекты DRM.</span><span class="sxs-lookup"><span data-stu-id="04b08-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="04b08-117">Эта функция требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, поддерживающие защищенные функции DRM.</span><span class="sxs-lookup"><span data-stu-id="04b08-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="04b08-118">**вмдрмшутдовн**</span><span class="sxs-lookup"><span data-stu-id="04b08-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="04b08-119">Высвобождает ресурсы, используемые интерфейсами API.</span><span class="sxs-lookup"><span data-stu-id="04b08-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="04b08-120">**вмдрмстартуп**</span><span class="sxs-lookup"><span data-stu-id="04b08-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="04b08-121">Инициализирует ресурсы, используемые интерфейсами API.</span><span class="sxs-lookup"><span data-stu-id="04b08-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="04b08-122">См. также</span><span class="sxs-lookup"><span data-stu-id="04b08-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04b08-123">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="04b08-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




