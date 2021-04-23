---
description: Класс Кбасеинпутпин является абстрактным базовым классом для реализации входных ПИН-кодов. Этот класс добавляет поддержку интерфейса Имеминпутпин в дополнение к поддержке интерфейса Ипин, предоставляемой Кбасепин.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Класс Кбасеинпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668623"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="04b16-104">Класс Кбасеинпутпин</span><span class="sxs-lookup"><span data-stu-id="04b16-104">CBaseInputPin class</span></span>

![Иерархия классов кбасеинпутпин](images/filter07.png)

<span data-ttu-id="04b16-106">`CBaseInputPin`Класс является абстрактным базовым классом для реализации входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="04b16-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="04b16-107">Этот класс добавляет поддержку интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) в дополнение к поддержке интерфейса [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) , предоставляемой [**кбасепин**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="04b16-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="04b16-108">Чтобы использовать этот класс, необходимо создать новый класс и переопределить по крайней мере следующие методы:</span><span class="sxs-lookup"><span data-stu-id="04b16-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="04b16-109">**Кбасеинпутпин:: Бегинфлуш**</span><span class="sxs-lookup"><span data-stu-id="04b16-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="04b16-110">**Кбасеинпутпин:: Ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="04b16-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="04b16-111">**Кбасеинпутпин:: Receive**</span><span class="sxs-lookup"><span data-stu-id="04b16-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="04b16-112">**Кбасепин:: Чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="04b16-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="04b16-113">**Кбасепин:: Жетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="04b16-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="04b16-114">В зависимости от функции ПИН-кода может потребоваться переопределить дополнительные методы в `CBaseInputPin` или **кбасепин**.</span><span class="sxs-lookup"><span data-stu-id="04b16-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="04b16-115">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="04b16-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="04b16-116">Описание</span><span class="sxs-lookup"><span data-stu-id="04b16-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04b16-117">**m \_ паллокатор**</span><span class="sxs-lookup"><span data-stu-id="04b16-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="04b16-118">Указатель на распределитель памяти.</span><span class="sxs-lookup"><span data-stu-id="04b16-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="04b16-119">**m \_ бреадонли**</span><span class="sxs-lookup"><span data-stu-id="04b16-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="04b16-120">Флаг, указывающий, создает ли распределитель образцы мультимедиа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="04b16-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="04b16-121">**m \_ бфлушинг**</span><span class="sxs-lookup"><span data-stu-id="04b16-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="04b16-122">Флаг, указывающий, выполняется ли сброс ПИН-кода в данный момент.</span><span class="sxs-lookup"><span data-stu-id="04b16-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="04b16-123">**m \_ самплепропс**</span><span class="sxs-lookup"><span data-stu-id="04b16-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="04b16-124">Свойства последнего примера.</span><span class="sxs-lookup"><span data-stu-id="04b16-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="04b16-125">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="04b16-125">Public Methods</span></span>                                                             | <span data-ttu-id="04b16-126">Описание</span><span class="sxs-lookup"><span data-stu-id="04b16-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="04b16-127">**кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="04b16-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="04b16-128">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="04b16-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="04b16-129">**~ Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="04b16-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="04b16-130">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="04b16-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="04b16-131">**бреакконнект**</span><span class="sxs-lookup"><span data-stu-id="04b16-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="04b16-132">Освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="04b16-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="04b16-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="04b16-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="04b16-134">Запрашивает, использует ли распределитель образцы мультимедиа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="04b16-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="04b16-135">**Запись на диск**</span><span class="sxs-lookup"><span data-stu-id="04b16-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="04b16-136">Запрашивает, выполняется ли в данный момент Очистка фильтра.</span><span class="sxs-lookup"><span data-stu-id="04b16-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="04b16-137">**чеккстреаминг**</span><span class="sxs-lookup"><span data-stu-id="04b16-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="04b16-138">Определяет, может ли ПИН-код принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="04b16-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="04b16-139">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="04b16-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="04b16-140">**пасснотифи**</span><span class="sxs-lookup"><span data-stu-id="04b16-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="04b16-141">Передает сообщение контроля качества соответствующему объекту.</span><span class="sxs-lookup"><span data-stu-id="04b16-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="04b16-142">**Неактивно**</span><span class="sxs-lookup"><span data-stu-id="04b16-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="04b16-143">Уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="04b16-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="04b16-144">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="04b16-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="04b16-145">**самплепропс**</span><span class="sxs-lookup"><span data-stu-id="04b16-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="04b16-146">Извлекает свойства последнего примера.</span><span class="sxs-lookup"><span data-stu-id="04b16-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="04b16-147">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="04b16-147">IPin Methods</span></span>                                                               | <span data-ttu-id="04b16-148">Описание</span><span class="sxs-lookup"><span data-stu-id="04b16-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="04b16-149">**бегинфлуш**</span><span class="sxs-lookup"><span data-stu-id="04b16-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="04b16-150">Начинает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="04b16-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="04b16-151">**ендфлуш**</span><span class="sxs-lookup"><span data-stu-id="04b16-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="04b16-152">Завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="04b16-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="04b16-153">Методы Имеминпутпин</span><span class="sxs-lookup"><span data-stu-id="04b16-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="04b16-154">Описание</span><span class="sxs-lookup"><span data-stu-id="04b16-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="04b16-155">**Распределителя**</span><span class="sxs-lookup"><span data-stu-id="04b16-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="04b16-156">Извлекает распределитель памяти, предложенный этим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="04b16-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="04b16-157">**нотифяллокатор**</span><span class="sxs-lookup"><span data-stu-id="04b16-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="04b16-158">Указывает распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="04b16-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="04b16-159">**жеталлокаторрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="04b16-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="04b16-160">Получает свойства распределителя, запрашиваемые входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="04b16-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="04b16-161">**Получать**</span><span class="sxs-lookup"><span data-stu-id="04b16-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="04b16-162">Получает следующий пример носителя в потоке.</span><span class="sxs-lookup"><span data-stu-id="04b16-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="04b16-163">**рецеивемултипле**</span><span class="sxs-lookup"><span data-stu-id="04b16-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="04b16-164">Получает несколько выборок в потоке.</span><span class="sxs-lookup"><span data-stu-id="04b16-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="04b16-165">**рецеивеканблокк**</span><span class="sxs-lookup"><span data-stu-id="04b16-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="04b16-166">Определяет, могут ли вызовы метода [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) блокироваться.</span><span class="sxs-lookup"><span data-stu-id="04b16-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="04b16-167">Методы Икуалитиконтрол</span><span class="sxs-lookup"><span data-stu-id="04b16-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="04b16-168">Описание</span><span class="sxs-lookup"><span data-stu-id="04b16-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="04b16-169">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="04b16-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="04b16-170">Получает сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="04b16-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="04b16-171">Требования</span><span class="sxs-lookup"><span data-stu-id="04b16-171">Requirements</span></span>



| <span data-ttu-id="04b16-172">Требование</span><span class="sxs-lookup"><span data-stu-id="04b16-172">Requirement</span></span> | <span data-ttu-id="04b16-173">Значение</span><span class="sxs-lookup"><span data-stu-id="04b16-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b16-174">Header</span><span class="sxs-lookup"><span data-stu-id="04b16-174">Header</span></span><br/>  | <dl> <span data-ttu-id="04b16-175"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04b16-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="04b16-176">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04b16-176">Library</span></span><br/> | <dl> <span data-ttu-id="04b16-177"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="04b16-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




