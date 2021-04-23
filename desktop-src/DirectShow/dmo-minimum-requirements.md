---
description: Минимальные требования DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Минимальные требования DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990182"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="f0968-103">Минимальные требования DMO</span><span class="sxs-lookup"><span data-stu-id="f0968-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="f0968-104">Каждый DMO должен соответствовать следующим минимальным требованиям:</span><span class="sxs-lookup"><span data-stu-id="f0968-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="f0968-105">Он должен поддерживать агрегирование.</span><span class="sxs-lookup"><span data-stu-id="f0968-105">It must support aggregation.</span></span>
-   <span data-ttu-id="f0968-106">Он должен предоставлять интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="f0968-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="f0968-107">Потоковая модель должна быть "both".</span><span class="sxs-lookup"><span data-stu-id="f0968-107">The threading model must be 'both'.</span></span> <span data-ttu-id="f0968-108">Дмос должен работать правильно в среде с свободной потоковой назначением.</span><span class="sxs-lookup"><span data-stu-id="f0968-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="f0968-109">Дмос Audio Effect должен поддерживать интерфейс [**имедиаобжектинплаце**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) для использования в DirectMusic и DirectSound.</span><span class="sxs-lookup"><span data-stu-id="f0968-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="f0968-110">Следующие интерфейсы описаны в других местах, но они полезны для многих дмос.</span><span class="sxs-lookup"><span data-stu-id="f0968-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="f0968-111">Однако они не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="f0968-111">They are not required, however.</span></span>

-   <span data-ttu-id="f0968-112">**ИспеЦифипропертипажес**, **ипропертипаже**. Эти интерфейсы позволяют DMO предоставить страницу свойств, чтобы пользователь установил свойства.</span><span class="sxs-lookup"><span data-stu-id="f0968-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="f0968-113">**IPersistStream**: этот интерфейс позволяет DMO сохранять свое состояние в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="f0968-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="f0968-114">[**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression). Эти интерфейсы позволяют клиенту настроить формат вывода кодировщика и параметры сжатия.</span><span class="sxs-lookup"><span data-stu-id="f0968-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="f0968-115">(Эти два интерфейса являются частью API DirectShow, но также рекомендуются для дмос.)</span><span class="sxs-lookup"><span data-stu-id="f0968-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0968-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f0968-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0968-117">Написание DMO</span><span class="sxs-lookup"><span data-stu-id="f0968-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



