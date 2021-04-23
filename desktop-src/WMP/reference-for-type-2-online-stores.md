---
title: Справочные материалы по интернет-магазинам типа 2
description: Справочные материалы по интернет-магазинам типа 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Интернет-магазины проигрывателя Windows Media, справочные материалы
- Интернет-магазины, справочные материалы
- Тип 2 Интернет-магазинов, справочные материалы
- Справочник по типам Интернет-магазинов типа 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789289"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="3c8df-107">Справочные материалы по интернет-магазинам типа 2</span><span class="sxs-lookup"><span data-stu-id="3c8df-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="3c8df-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="3c8df-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3c8df-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c8df-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3c8df-110">Проигрыватель Windows Media 10 или более поздней версии предоставляет объекты, интерфейсы, свойства и методы, поддерживающие Интернет-магазины типа 2.</span><span class="sxs-lookup"><span data-stu-id="3c8df-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="3c8df-111">Эти сведения подробно описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="3c8df-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="3c8df-112">Section</span><span class="sxs-lookup"><span data-stu-id="3c8df-112">Section</span></span>                                                                                                        | <span data-ttu-id="3c8df-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3c8df-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c8df-114">Интерфейс Ивмпсубскриптионсервице</span><span class="sxs-lookup"><span data-stu-id="3c8df-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="3c8df-115">Предоставляет методы для расширения управления цифровыми правами (DRM) и инициирования фоновых процессов.</span><span class="sxs-lookup"><span data-stu-id="3c8df-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="3c8df-116">Интерфейс IWMPSubscriptionService2</span><span class="sxs-lookup"><span data-stu-id="3c8df-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="3c8df-117">Предоставляет методы для инициации фоновых процессов, предоставления сведений о работе Интернет-магазина и предоставления указателя на основной интерфейс проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3c8df-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="3c8df-118">Интерфейс Ивмпсубскриптионсервицекаллбакк</span><span class="sxs-lookup"><span data-stu-id="3c8df-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="3c8df-119">Определяет метод, используемый в Интернет-магазинах для уведомления проигрывателя Windows Media о завершении фонового процесса.</span><span class="sxs-lookup"><span data-stu-id="3c8df-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="3c8df-120">вмпнотифисубскриптионплугинаддремове</span><span class="sxs-lookup"><span data-stu-id="3c8df-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="3c8df-121">Функция, используемая для уведомления проигрывателя Windows Media о том, что подключаемый модуль установлен или удален.</span><span class="sxs-lookup"><span data-stu-id="3c8df-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="3c8df-122">Объект Довнлоадколлектион</span><span class="sxs-lookup"><span data-stu-id="3c8df-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="3c8df-123">Предоставляет методы и свойства для управления коллекциями элементов загрузки.</span><span class="sxs-lookup"><span data-stu-id="3c8df-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="3c8df-124">Объект Довнлоадитем</span><span class="sxs-lookup"><span data-stu-id="3c8df-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="3c8df-125">Предоставляет методы и свойства, относящиеся к запросам на загрузку.</span><span class="sxs-lookup"><span data-stu-id="3c8df-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="3c8df-126">Объект Довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="3c8df-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="3c8df-127">Предоставляет методы для управления коллекциями загрузки.</span><span class="sxs-lookup"><span data-stu-id="3c8df-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="3c8df-128">Внешний объект для Интернет-магазинов типа 2</span><span class="sxs-lookup"><span data-stu-id="3c8df-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="3c8df-129">Предоставляет свойства, методы и событие, доступное из веб-страниц Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="3c8df-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="3c8df-130">Перечисления для Интернет-магазинов типа 2</span><span class="sxs-lookup"><span data-stu-id="3c8df-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="3c8df-131">Описывает перечисления, используемые Интернет-магазинами.</span><span class="sxs-lookup"><span data-stu-id="3c8df-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="3c8df-132">Соглашение о задании BITS проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="3c8df-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="3c8df-133">Описывает соглашение об использовании фоновая интеллектуальная служба передачи (BITS).</span><span class="sxs-lookup"><span data-stu-id="3c8df-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="3c8df-134">Разделы реестра и записи для Интернет-магазина типа 2</span><span class="sxs-lookup"><span data-stu-id="3c8df-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="3c8df-135">Описывает записи реестра, которые Интернет-магазин должен создать в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c8df-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="3c8df-136">См. также</span><span class="sxs-lookup"><span data-stu-id="3c8df-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8df-137">**Тип 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="3c8df-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




