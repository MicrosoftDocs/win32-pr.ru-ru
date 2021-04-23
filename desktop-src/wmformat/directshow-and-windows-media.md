---
title: DirectShow и Windows Media
description: DirectShow и Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779751"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="daefd-107">DirectShow и Windows Media</span><span class="sxs-lookup"><span data-stu-id="daefd-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="daefd-108">В качестве альтернативы эксклюзивному использованию пакета SDK формата Windows Media приложения могут также считывать и записывать содержимое Windows Media, используя архитектуру Microsoft® DirectShow® потоковой передачи, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="daefd-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="daefd-109">Section</span><span class="sxs-lookup"><span data-stu-id="daefd-109">Section</span></span>                                                                                   | <span data-ttu-id="daefd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="daefd-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="daefd-111">О DirectShow</span><span class="sxs-lookup"><span data-stu-id="daefd-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="daefd-112">Описание DirectShow в общих чертах и сведения о месте получения дополнительных сведений о ней.</span><span class="sxs-lookup"><span data-stu-id="daefd-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="daefd-113">Зачем использовать DirectShow?</span><span class="sxs-lookup"><span data-stu-id="daefd-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="daefd-114">Описывает, как DirectShow упрощает определенные задачи при создании и воспроизведении содержимого на основе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="daefd-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="daefd-115">Чтение файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="daefd-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="daefd-116">Описывает, как воспроизводить файлы ASF с помощью DirectShow.</span><span class="sxs-lookup"><span data-stu-id="daefd-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="daefd-117">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="daefd-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="daefd-118">Описывает создание файлов ASF с помощью DirectShow.</span><span class="sxs-lookup"><span data-stu-id="daefd-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="daefd-119">\_Уведомление о событии состояния ВМТ в DirectShow</span><span class="sxs-lookup"><span data-stu-id="daefd-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="daefd-120">Описывает, какие события **\_ состояния ВМТ** обрабатываются фильтрами модуля чтения ASF и модулем записи ASF, и как приложения могут получить эти события.</span><span class="sxs-lookup"><span data-stu-id="daefd-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="daefd-121">Поддержка DRM в DirectShow</span><span class="sxs-lookup"><span data-stu-id="daefd-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="daefd-122">Описывает чтение и запись защищенных DRM файлов с помощью DirectShow.</span><span class="sxs-lookup"><span data-stu-id="daefd-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="daefd-123">Справочник по КАСФ DirectShow</span><span class="sxs-lookup"><span data-stu-id="daefd-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="daefd-124">Содержит справочную документацию по компонентам DirectShow, поддерживающим Windows Media.</span><span class="sxs-lookup"><span data-stu-id="daefd-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="daefd-125">Три примера приложений в пакете SDK иллюстрируют использование DirectShow: Дскопи, Дсплай и Дссикфм.</span><span class="sxs-lookup"><span data-stu-id="daefd-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="daefd-126">Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="daefd-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="daefd-127">Для приложений, использующих компоненты КАСФ, включенные в этот пакет SDK, необходимо установить Microsoft DirectX® 8,1 или более поздней версии пакета SDK для Windows® 2000, Windows 98 и Windows 95 Systems.</span><span class="sxs-lookup"><span data-stu-id="daefd-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="daefd-128">В частности, эта среда выполнения необходима для фильтра оболочки DMO, который размещает кодеки Windows Media в графе фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="daefd-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 




