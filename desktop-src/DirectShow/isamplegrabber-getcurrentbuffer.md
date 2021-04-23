---
description: Метод Жеткуррентбуффер извлекает копию буфера, связанную с последним примером.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Метод Исамплеграббер:: Жеткуррентбуффер (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675956"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="dfc15-103">Метод Исамплеграббер:: Жеткуррентбуффер</span><span class="sxs-lookup"><span data-stu-id="dfc15-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="dfc15-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="dfc15-104">\[Deprecated.</span></span> <span data-ttu-id="dfc15-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dfc15-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dfc15-106">Метод **жеткуррентбуффер** извлекает копию буфера, связанную с последним примером.</span><span class="sxs-lookup"><span data-stu-id="dfc15-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc15-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfc15-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="dfc15-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfc15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc15-109">*пбуфферсизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dfc15-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc15-110">Указатель на размер буфера.</span><span class="sxs-lookup"><span data-stu-id="dfc15-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="dfc15-111">Если *pBuffer* имеет **значение NULL**, этот параметр получает требуемый размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="dfc15-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="dfc15-112">Если *pBuffer* не равно **null**, установите этот параметр равным размеру буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="dfc15-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="dfc15-113">В выходных данных параметр получает число байтов, скопированных в буфер.</span><span class="sxs-lookup"><span data-stu-id="dfc15-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="dfc15-114">Это значение может быть меньше, чем размер буфера.</span><span class="sxs-lookup"><span data-stu-id="dfc15-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dfc15-115">*pBuffer* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfc15-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc15-116">Указатель на массив байтов размера *пбуфферсизе* или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfc15-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="dfc15-117">Если этот параметр не равен **null**, текущий буфер копируется в массив.</span><span class="sxs-lookup"><span data-stu-id="dfc15-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="dfc15-118">Если этот параметр имеет **значение NULL**, параметр *пбуфферсизе* получает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="dfc15-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc15-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfc15-119">Return value</span></span>

<span data-ttu-id="dfc15-120">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dfc15-120">Returns one of the following values.</span></span>



| <span data-ttu-id="dfc15-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dfc15-121">Return code</span></span>                                                                                           | <span data-ttu-id="dfc15-122">Описание</span><span class="sxs-lookup"><span data-stu-id="dfc15-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfc15-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="dfc15-124">Образцы не буферизуются.</span><span class="sxs-lookup"><span data-stu-id="dfc15-124">Samples are not being buffered.</span></span> <span data-ttu-id="dfc15-125">Вызовите [**исамплеграббер:: сетбуфферсамплес**](isamplegrabber-setbuffersamples.md).</span><span class="sxs-lookup"><span data-stu-id="dfc15-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="dfc15-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="dfc15-127">Указанный буфер недостаточно велик.</span><span class="sxs-lookup"><span data-stu-id="dfc15-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="dfc15-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="dfc15-129">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="dfc15-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="dfc15-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="dfc15-131">Успешно.</span><span class="sxs-lookup"><span data-stu-id="dfc15-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="dfc15-132"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dfc15-133">Фильтр не подключен.</span><span class="sxs-lookup"><span data-stu-id="dfc15-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="dfc15-134"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="dfc15-135">Фильтр еще не получил выборки.</span><span class="sxs-lookup"><span data-stu-id="dfc15-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="dfc15-136">Чтобы предоставить пример, запустите или приостановите граф.</span><span class="sxs-lookup"><span data-stu-id="dfc15-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="dfc15-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfc15-137">Remarks</span></span>

<span data-ttu-id="dfc15-138">Чтобы активировать буферизацию, вызовите [**исамплеграббер:: сетбуфферсамплес**](isamplegrabber-setbuffersamples.md) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="dfc15-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="dfc15-139">Вызовите этот метод дважды.</span><span class="sxs-lookup"><span data-stu-id="dfc15-139">Call this method twice.</span></span> <span data-ttu-id="dfc15-140">При первом вызове задайте для *PBuffer* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfc15-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="dfc15-141">Размер буфера возвращается в *пбуфферсизе*.</span><span class="sxs-lookup"><span data-stu-id="dfc15-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="dfc15-142">Затем выделите массив и снова вызовите метод.</span><span class="sxs-lookup"><span data-stu-id="dfc15-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="dfc15-143">Во втором вызове передайте размер массива в *пбуфферсизе* и передайте адрес массива в *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="dfc15-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="dfc15-144">Если массив недостаточно велик, метод возвращает E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dfc15-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="dfc15-145">Параметр *pBuffer* типизирован как **длинный** указатель, но содержимое буфера зависит от формата данных.</span><span class="sxs-lookup"><span data-stu-id="dfc15-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="dfc15-146">Вызовите метод [**исамплеграббер:: жетконнектедмедиатипе**](isamplegrabber-getconnectedmediatype.md) , чтобы получить тип мультимедиа формата.</span><span class="sxs-lookup"><span data-stu-id="dfc15-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="dfc15-147">Не вызывайте этот метод во время работы графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="dfc15-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="dfc15-148">Пока граф фильтра работает, фильтр захвата при каждом получении нового образца переписывает содержимое буфера.</span><span class="sxs-lookup"><span data-stu-id="dfc15-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="dfc15-149">Лучший способ использовать этот метод — использовать Однофакторный режим, который останавливает граф после получения первого образца.</span><span class="sxs-lookup"><span data-stu-id="dfc15-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="dfc15-150">Чтобы задать Однофакторный режим, вызовите метод [**исамплеграббер:: сетонешот**](isamplegrabber-setoneshot.md).</span><span class="sxs-lookup"><span data-stu-id="dfc15-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="dfc15-151">Фильтр не содержит образцов предварительной подсчета или выборки, в которых элемент **двстреамид** структуры [**\_ \_ свойств SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) отличается от \_ потока \_ мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dfc15-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="dfc15-152">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="dfc15-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dfc15-153">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dfc15-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dfc15-154">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dfc15-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dfc15-155">Требования</span><span class="sxs-lookup"><span data-stu-id="dfc15-155">Requirements</span></span>



| <span data-ttu-id="dfc15-156">Требование</span><span class="sxs-lookup"><span data-stu-id="dfc15-156">Requirement</span></span> | <span data-ttu-id="dfc15-157">Значение</span><span class="sxs-lookup"><span data-stu-id="dfc15-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc15-158">Header</span><span class="sxs-lookup"><span data-stu-id="dfc15-158">Header</span></span><br/>  | <dl> <span data-ttu-id="dfc15-159"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dfc15-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dfc15-160">Library</span></span><br/> | <dl> <span data-ttu-id="dfc15-161"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfc15-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc15-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfc15-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc15-163">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="dfc15-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="dfc15-164">**Интерфейс Исамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="dfc15-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




