---
description: Класс Ксаурце является базовым классом для реализации фильтров источника. Фильтр, производный от Ксаурце, содержит один или несколько выходных закрепления, производных от класса Ксаурцестреам. Каждый выходной ПИН-код создает рабочий поток, который передает образцы мультимедиа в нисходящий.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Класс Ксаурце (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688954"
---
# <a name="csource-class"></a><span data-ttu-id="f59e7-105">Класс Ксаурце</span><span class="sxs-lookup"><span data-stu-id="f59e7-105">CSource class</span></span>

![Иерархия классов ксаурце](images/source01.png)

<span data-ttu-id="f59e7-107">Класс **ксаурце** является базовым классом для реализации фильтров источника.</span><span class="sxs-lookup"><span data-stu-id="f59e7-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="f59e7-108">Фильтр, производный от **ксаурце** , содержит один или несколько выходных закрепления, производных от класса [**ксаурцестреам**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="f59e7-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="f59e7-109">Каждый выходной ПИН-код создает рабочий поток, который передает образцы мультимедиа в нисходящий.</span><span class="sxs-lookup"><span data-stu-id="f59e7-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="f59e7-110">Класс **ксаурце** предназначен для поддержки модели push-уведомлений для потока данных.</span><span class="sxs-lookup"><span data-stu-id="f59e7-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="f59e7-111">Этот класс не рекомендуется для создания фильтров чтения файлов.</span><span class="sxs-lookup"><span data-stu-id="f59e7-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="f59e7-112">Модули чтения файлов должны поддерживать модель извлечения через интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="f59e7-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="f59e7-113">Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f59e7-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="f59e7-114">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="f59e7-114">Protected Member Variables</span></span>                     | <span data-ttu-id="f59e7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f59e7-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f59e7-116">**m \_ ипинс**</span><span class="sxs-lookup"><span data-stu-id="f59e7-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="f59e7-117">Количество ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="f59e7-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="f59e7-118">**m \_ пастреамс**</span><span class="sxs-lookup"><span data-stu-id="f59e7-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="f59e7-119">Массив ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="f59e7-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="f59e7-120">**m \_ кстателокк**</span><span class="sxs-lookup"><span data-stu-id="f59e7-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="f59e7-121">Объект критического раздела, защищающий состояние фильтра.</span><span class="sxs-lookup"><span data-stu-id="f59e7-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="f59e7-122">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="f59e7-122">Public Methods</span></span>                                 | <span data-ttu-id="f59e7-123">Описание</span><span class="sxs-lookup"><span data-stu-id="f59e7-123">Description</span></span>                                                  |
| [<span data-ttu-id="f59e7-124">**ксаурце**</span><span class="sxs-lookup"><span data-stu-id="f59e7-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="f59e7-125">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f59e7-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="f59e7-126">**~ Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="f59e7-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="f59e7-127">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="f59e7-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="f59e7-128">**жетпинкаунт**</span><span class="sxs-lookup"><span data-stu-id="f59e7-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="f59e7-129">Возвращает количество ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="f59e7-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="f59e7-130">**жетпин**</span><span class="sxs-lookup"><span data-stu-id="f59e7-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="f59e7-131">Извлекает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="f59e7-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="f59e7-132">**пстателокк**</span><span class="sxs-lookup"><span data-stu-id="f59e7-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="f59e7-133">Извлекает указатель на объект критической секции фильтра.</span><span class="sxs-lookup"><span data-stu-id="f59e7-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="f59e7-134">**аддпин**</span><span class="sxs-lookup"><span data-stu-id="f59e7-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="f59e7-135">Добавляет новый выходной ПИН-код в фильтр.</span><span class="sxs-lookup"><span data-stu-id="f59e7-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="f59e7-136">**ремовепин**</span><span class="sxs-lookup"><span data-stu-id="f59e7-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="f59e7-137">Удаляет указанный ПИН-код из фильтра.</span><span class="sxs-lookup"><span data-stu-id="f59e7-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="f59e7-138">**финдпиннумбер**</span><span class="sxs-lookup"><span data-stu-id="f59e7-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="f59e7-139">Возвращает номер указанного пин-кода для фильтра.</span><span class="sxs-lookup"><span data-stu-id="f59e7-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="f59e7-140">Методы Ибасефилтер</span><span class="sxs-lookup"><span data-stu-id="f59e7-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="f59e7-141">Описание</span><span class="sxs-lookup"><span data-stu-id="f59e7-141">Description</span></span>                                                  |
| [<span data-ttu-id="f59e7-142">**финдпин**</span><span class="sxs-lookup"><span data-stu-id="f59e7-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="f59e7-143">Извлекает ПИН-код с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="f59e7-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="f59e7-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f59e7-144">Remarks</span></span>

<span data-ttu-id="f59e7-145">Чтобы реализовать выходной ПИН-код, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f59e7-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="f59e7-146">Создайте класс, производный от [**ксаурцестреам**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="f59e7-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="f59e7-147">Переопределите метод [**ксаурцестреам:: жетмедиатипе**](csourcestream-getmediatype.md) и, возможно, метод [**Ксаурцестреам:: чеккмедиатипе**](csourcestream-checkmediatype.md) , который проверяет типы носителей для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="f59e7-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="f59e7-148">Реализуйте метод [**кбасеаутпутпин::D еЦидебуфферсизе**](cbaseoutputpin-decidebuffersize.md) , который возвращает требования к буферу ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="f59e7-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="f59e7-149">Реализуйте метод [**ксаурцестреам:: филлбуффер**](csourcestream-fillbuffer.md) , который заполняет буфер образца мультимедиа данными.</span><span class="sxs-lookup"><span data-stu-id="f59e7-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="f59e7-150">Чтобы реализовать фильтр, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f59e7-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="f59e7-151">Создайте класс, производный от **ксаурце**.</span><span class="sxs-lookup"><span data-stu-id="f59e7-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="f59e7-152">В конструкторе создайте один или несколько выходных закрепления, полученных из [**ксаурцестреам**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="f59e7-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="f59e7-153">ПИН-коды автоматически добавляются в фильтр в своих методах-конструкторах и удаляются в своих методах-деструкторах.</span><span class="sxs-lookup"><span data-stu-id="f59e7-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="f59e7-154">Чтобы синхронизировать состояние фильтра между несколькими потоками, вызовите метод [**ксаурце::P стателокк**](csource--pstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="f59e7-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="f59e7-155">Этот метод возвращает указатель на раздел критического состояния фильтра.</span><span class="sxs-lookup"><span data-stu-id="f59e7-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="f59e7-156">Используйте класс [**каутолокк**](cautolock.md) для хранения критической секции.</span><span class="sxs-lookup"><span data-stu-id="f59e7-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="f59e7-157">Из ПИН-кода можно получить доступ к **пстателокк** из переменной-члена [**кбасепин:: \_ m**](cbasepin-m-pfilter.md) закрепления, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="f59e7-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="f59e7-158">Требования</span><span class="sxs-lookup"><span data-stu-id="f59e7-158">Requirements</span></span>



| <span data-ttu-id="f59e7-159">Требование</span><span class="sxs-lookup"><span data-stu-id="f59e7-159">Requirement</span></span> | <span data-ttu-id="f59e7-160">Значение</span><span class="sxs-lookup"><span data-stu-id="f59e7-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f59e7-161">Header</span><span class="sxs-lookup"><span data-stu-id="f59e7-161">Header</span></span><br/>  | <dl> <span data-ttu-id="f59e7-162"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f59e7-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f59e7-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f59e7-163">Library</span></span><br/> | <dl> <span data-ttu-id="f59e7-164"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f59e7-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59e7-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f59e7-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59e7-166">Запись фильтров источника</span><span class="sxs-lookup"><span data-stu-id="f59e7-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




