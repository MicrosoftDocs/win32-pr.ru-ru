---
description: Интерфейс Иамтимелинекомп вставляет или извлекает Виртуальные дорожки в композиции в службах редактирования DirectShow (DES). Композиция — это коллекция слоев, которая выступает в качестве отдельной составной записи.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Интерфейс Иамтимелинекомп (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680076"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="51b38-103">Интерфейс Иамтимелинекомп</span><span class="sxs-lookup"><span data-stu-id="51b38-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="51b38-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="51b38-104">\[Deprecated.</span></span> <span data-ttu-id="51b38-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51b38-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51b38-106">Интерфейс **иамтимелинекомп** вставляет или извлекает Виртуальные дорожки в композиции в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="51b38-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="51b38-107">Композиция — это коллекция слоев, которая выступает в качестве отдельной составной *записи*. Например, композиция, которая содержит две дорожки с переходом между ними, действует как единая дорожка с предкомпозициым переходом.</span><span class="sxs-lookup"><span data-stu-id="51b38-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="51b38-108">Композиция должна содержать носители только одного типа (например, аудио или видео), но это ограничение не применяется.</span><span class="sxs-lookup"><span data-stu-id="51b38-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="51b38-109">*Виртуальная дорожка* — это любой объект, который может находиться в композиции, включая записи и другие композиции.</span><span class="sxs-lookup"><span data-stu-id="51b38-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="51b38-110">Самые верхние узлы на временной шкале являются *группами*.</span><span class="sxs-lookup"><span data-stu-id="51b38-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="51b38-111">Группы реализуют `IAMTimelineComp` интерфейс и интерфейс [**иамтимелинеграуп**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="51b38-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="51b38-112">Чтобы создать объект композиции, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) со значением, \_ составляющим основной тип временной шкалы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="51b38-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="51b38-113">Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для `IAMTimelineComp` интерфейса.</span><span class="sxs-lookup"><span data-stu-id="51b38-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="51b38-114">Дополнительные сведения см. [в разделе Модель временной шкалы](the-timeline-model.md) и [Построение временной шкалы](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="51b38-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="51b38-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="51b38-115">Members</span></span>

<span data-ttu-id="51b38-116">Интерфейс **иамтимелинекомп** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="51b38-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="51b38-117">**Иамтимелинекомп** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="51b38-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="51b38-118">Методы</span><span class="sxs-lookup"><span data-stu-id="51b38-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="51b38-119">Методы</span><span class="sxs-lookup"><span data-stu-id="51b38-119">Methods</span></span>

<span data-ttu-id="51b38-120">Интерфейс **иамтимелинекомп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="51b38-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="51b38-121">Метод</span><span class="sxs-lookup"><span data-stu-id="51b38-121">Method</span></span>                                                                       | <span data-ttu-id="51b38-122">Описание</span><span class="sxs-lookup"><span data-stu-id="51b38-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51b38-123">**жеткаунтофтипе**</span><span class="sxs-lookup"><span data-stu-id="51b38-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="51b38-124">Извлекает количество объектов заданного типа, содержащихся в этой композиции, и всех ее виртуальных дорожек рекурсивно.</span><span class="sxs-lookup"><span data-stu-id="51b38-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="51b38-125">**жетнекствтракк**</span><span class="sxs-lookup"><span data-stu-id="51b38-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="51b38-126">Извлекает следующую виртуальную запись после указанной виртуальной записи.</span><span class="sxs-lookup"><span data-stu-id="51b38-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="51b38-127">**жетрекурсивелайерофтипе**</span><span class="sxs-lookup"><span data-stu-id="51b38-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="51b38-128">Выполняет упорядочение по глубине виртуальных дорожек, содержащихся в этой композиции, и извлекает из этого упорядочения *n*-й виртуальный объект Track.</span><span class="sxs-lookup"><span data-stu-id="51b38-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="51b38-129">**жетрекурсивелайерофтипеи**</span><span class="sxs-lookup"><span data-stu-id="51b38-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="51b38-130">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="51b38-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="51b38-131">**жетвтракк**</span><span class="sxs-lookup"><span data-stu-id="51b38-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="51b38-132">Извлекает виртуальную дорожку по указанному приоритету.</span><span class="sxs-lookup"><span data-stu-id="51b38-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="51b38-133">**втраккжеткаунт**</span><span class="sxs-lookup"><span data-stu-id="51b38-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="51b38-134">Возвращает число виртуальных дорожек, содержащихся в композиции.</span><span class="sxs-lookup"><span data-stu-id="51b38-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="51b38-135">**втраккинсбефоре**</span><span class="sxs-lookup"><span data-stu-id="51b38-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="51b38-136">Вставляет виртуальную дорожку в композицию по заданному приоритету.</span><span class="sxs-lookup"><span data-stu-id="51b38-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="51b38-137">**втракксвапприоритиес**</span><span class="sxs-lookup"><span data-stu-id="51b38-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="51b38-138">Переключает уровни приоритета двух дорожек.</span><span class="sxs-lookup"><span data-stu-id="51b38-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="51b38-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51b38-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="51b38-140">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="51b38-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="51b38-141">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="51b38-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="51b38-142">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="51b38-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51b38-143">Требования</span><span class="sxs-lookup"><span data-stu-id="51b38-143">Requirements</span></span>



| <span data-ttu-id="51b38-144">Требование</span><span class="sxs-lookup"><span data-stu-id="51b38-144">Requirement</span></span> | <span data-ttu-id="51b38-145">Значение</span><span class="sxs-lookup"><span data-stu-id="51b38-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51b38-146">Header</span><span class="sxs-lookup"><span data-stu-id="51b38-146">Header</span></span><br/>  | <dl> <span data-ttu-id="51b38-147"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b38-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="51b38-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51b38-148">Library</span></span><br/> | <dl> <span data-ttu-id="51b38-149"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51b38-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
