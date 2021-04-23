---
description: Добавление эффектов и объектов перехода
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Добавление эффектов и объектов перехода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072208"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="5d49f-103">Добавление эффектов и объектов перехода</span><span class="sxs-lookup"><span data-stu-id="5d49f-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="5d49f-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="5d49f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5d49f-105">В DES результат или переход представлен двумя объектами:</span><span class="sxs-lookup"><span data-stu-id="5d49f-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="5d49f-106">*Объект временной шкалы* представляет собой результат или переход в пределах временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="5d49f-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="5d49f-107">Для эффектов объект временной шкалы поддерживает интерфейс [**иамтимелиниффект**](iamtimelineeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="5d49f-108">Для переходов он поддерживает интерфейс [**иамтимелинетранс**](iamtimelinetrans.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="5d49f-109">Оба типа поддерживают интерфейс [**иамтимелинеобж**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="5d49f-110">*Подобъект* — это объект, который реализует обработку данных для данного действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="5d49f-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="5d49f-111">Объект временной шкалы содержит указатель на подобъект.</span><span class="sxs-lookup"><span data-stu-id="5d49f-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="5d49f-112">Чтобы добавить действие или переход, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5d49f-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="5d49f-113">**1. Создание объекта временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="5d49f-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="5d49f-114">Чтобы создать объект временной шкалы, вызовите метод [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="5d49f-115">Задайте для какого-либо действия тип, равный **\_ основному \_ типу \_ временной шкалы** , или **\_ \_ \_ смену основного типа временной шкалы** для перехода.</span><span class="sxs-lookup"><span data-stu-id="5d49f-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="5d49f-116">В следующем примере создается объект перехода.</span><span class="sxs-lookup"><span data-stu-id="5d49f-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="5d49f-117">**2. Указание подобъекта**</span><span class="sxs-lookup"><span data-stu-id="5d49f-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="5d49f-118">Объект временной шкалы выступает в качестве оболочки для другого объекта, называемого *подобъектом*, который выполняет реальную работу.</span><span class="sxs-lookup"><span data-stu-id="5d49f-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="5d49f-119">Подобъект реализует преобразование данных, которое создает нужный результат или переход.</span><span class="sxs-lookup"><span data-stu-id="5d49f-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="5d49f-120">Список переходов и эффектов, предоставляемых DES, см. в разделе [переходы и эффекты](transitions-and-effects.md).</span><span class="sxs-lookup"><span data-stu-id="5d49f-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="5d49f-121">Чтобы задать подобъект, вызовите метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) для объекта Timeline, передав ему идентификатор класса (CLSID) подобъекта.</span><span class="sxs-lookup"><span data-stu-id="5d49f-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="5d49f-122">DirectShow предоставляет перечислитель для видеоэффектов и видеопереходов, которые можно использовать для получения идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="5d49f-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="5d49f-123">Дополнительные сведения см. в разделе [перечисление эффектов и переходов](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="5d49f-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="5d49f-124">В следующем примере в качестве подобъекта задается [Переход на очистку SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="5d49f-125">**3. Задание времени начала и окончания**</span><span class="sxs-lookup"><span data-stu-id="5d49f-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="5d49f-126">Чтобы задать время начала и окончания, вызовите метод [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="5d49f-127">Эти значения времени задаются относительно времени начала родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="5d49f-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="5d49f-128">Эффекты могут пересекаться в пределах одного объекта, но переходы не могут.</span><span class="sxs-lookup"><span data-stu-id="5d49f-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="5d49f-129">В следующем примере время начала устанавливается равным 5 секундам, а время окончания — 10 секундам:</span><span class="sxs-lookup"><span data-stu-id="5d49f-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="5d49f-130">При подготовке к просмотру ход перехода в каждом кадре вычисляется на основе свойства **Progress** , которое нормализовано до диапазона от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="5d49f-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="5d49f-131">DES использует время начала каждого кадра для вычисления значения хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="5d49f-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="5d49f-132">Это означает, что если время прекращения перехода равно значению времени прекращения источника, то значение **хода выполнения** никогда не достигнет ровно 1,0, так как время начала последнего кадра немного, чем время окончания.</span><span class="sxs-lookup"><span data-stu-id="5d49f-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="5d49f-133">Чтобы переход был достигнут до 1,0, установите время окончания перехода как минимум на один кадр, который раньше, чем время окончания источника.</span><span class="sxs-lookup"><span data-stu-id="5d49f-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="5d49f-134">**4. Вставка объекта на временную шкалу**</span><span class="sxs-lookup"><span data-stu-id="5d49f-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="5d49f-135">Чтобы вставить объект на временную шкалу, вызовите один из следующих методов родительского элемента, в зависимости от типа объекта:</span><span class="sxs-lookup"><span data-stu-id="5d49f-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="5d49f-136">Эффекты: [ **иамтимелиниффектабле:: еффектинсбефоре**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="5d49f-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="5d49f-137">Переходы: [ **иамтимелинетрансабле:: трансадд**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="5d49f-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="5d49f-138">В методе [**иамтимелиниффектабле:: еффектинсбефоре**](iamtimelineeffectable-effectinsbefore.md) необходимо указать приоритет этого действия.</span><span class="sxs-lookup"><span data-stu-id="5d49f-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="5d49f-139">Когда эффекты перекрываются для одного и того же объекта, они применяются в порядке приоритета.</span><span class="sxs-lookup"><span data-stu-id="5d49f-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="5d49f-140">Звуковым результатом конверта тома является исключение. Дополнительные сведения см. в справочнике по [эффекты конверта тома](volume-envelope-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="5d49f-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="5d49f-141">В составе композиции все звуковые дорожки смешиваются до применения звуковых эффектов для этой композиции.</span><span class="sxs-lookup"><span data-stu-id="5d49f-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="5d49f-142">Поскольку переходы не могут перекрывать один и тот же объект, они не имеют значения приоритета.</span><span class="sxs-lookup"><span data-stu-id="5d49f-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="5d49f-143">В следующем примере объект перехода добавляется к дорожке:</span><span class="sxs-lookup"><span data-stu-id="5d49f-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="5d49f-144">В примере запрашивается объект Track для интерфейса [**иамтимелинетрансабле**](iamtimelinetransable.md) перед вызовом аддтранс.</span><span class="sxs-lookup"><span data-stu-id="5d49f-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="5d49f-145">**5. Задание свойств**</span><span class="sxs-lookup"><span data-stu-id="5d49f-145">**5. Set Properties**</span></span>

<span data-ttu-id="5d49f-146">Многие эффекты и переходы поддерживают пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="5d49f-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="5d49f-147">Дополнительные сведения см. [в разделе Задание свойств для эффектов и переходов](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="5d49f-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="5d49f-148">Пример</span><span class="sxs-lookup"><span data-stu-id="5d49f-148">Example</span></span>

<span data-ttu-id="5d49f-149">В следующем примере кода добавляется [Переход SMPTE очистки](smpte-wipe-transition.md) к дорожке. Предполагается, что объект Track уже существует на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="5d49f-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="5d49f-150">См. также</span><span class="sxs-lookup"><span data-stu-id="5d49f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d49f-151">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="5d49f-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



