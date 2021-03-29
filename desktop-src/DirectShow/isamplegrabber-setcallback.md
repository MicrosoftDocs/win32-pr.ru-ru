---
description: Метод Сеткаллбакк задает метод обратного вызова для вызова входящих образцов.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Метод Исамплеграббер:: Сеткаллбакк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675954"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="cfc1b-103">Метод Исамплеграббер:: Сеткаллбакк</span><span class="sxs-lookup"><span data-stu-id="cfc1b-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="cfc1b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-104">\[Deprecated.</span></span> <span data-ttu-id="cfc1b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cfc1b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cfc1b-106">Метод **сеткаллбакк** задает метод обратного вызова для вызова входящих образцов.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc1b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfc1b-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="cfc1b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfc1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc1b-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="cfc1b-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc1b-110">Указатель на интерфейс [**исамплеграбберкб**](isamplegrabbercb.md) , содержащий метод обратного вызова, или **значение NULL** для отмены обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="cfc1b-111">*вхичмесодтокаллбакк*</span><span class="sxs-lookup"><span data-stu-id="cfc1b-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc1b-112">Индекс, указывающий метод обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-112">Index specifying the callback method.</span></span> <span data-ttu-id="cfc1b-113">Должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-113">Must be one of the following values.</span></span>



| <span data-ttu-id="cfc1b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc1b-114">Value</span></span> | <span data-ttu-id="cfc1b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cfc1b-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc1b-116">0</span><span class="sxs-lookup"><span data-stu-id="cfc1b-116">0</span></span>     | <span data-ttu-id="cfc1b-117">Образец фильтра захвата вызывает метод [**исамплеграбберкб:: самплекб**](isamplegrabbercb-samplecb.md) .</span><span class="sxs-lookup"><span data-stu-id="cfc1b-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="cfc1b-118">Этот метод получает указатель [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="cfc1b-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="cfc1b-119">1</span><span class="sxs-lookup"><span data-stu-id="cfc1b-119">1</span></span>     | <span data-ttu-id="cfc1b-120">Образец фильтра захвата вызывает метод [**исамплеграбберкб:: буфферкб**](isamplegrabbercb-buffercb.md) .</span><span class="sxs-lookup"><span data-stu-id="cfc1b-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="cfc1b-121">Этот метод получает указатель на буфер, содержащийся в примере носителя.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc1b-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfc1b-122">Return value</span></span>

<span data-ttu-id="cfc1b-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cfc1b-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cfc1b-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc1b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfc1b-125">Remarks</span></span>

<span data-ttu-id="cfc1b-126">Поток обработки данных блокируется до тех пор, пока метод обратного вызова не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="cfc1b-127">Если обратный вызов не возвращает быстрое значение, он может помешать воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="cfc1b-128">Фильтр не вызывает функцию обратного вызова для предварительных образцов или для образцов, в которых элемент **двстреамид** структуры [**\_ \_ свойств SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) не является \_ потоком \_ мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="cfc1b-129">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cfc1b-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cfc1b-130">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfc1b-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cfc1b-131">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cfc1b-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfc1b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="cfc1b-132">Requirements</span></span>



| <span data-ttu-id="cfc1b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="cfc1b-133">Requirement</span></span> | <span data-ttu-id="cfc1b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc1b-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc1b-135">Header</span><span class="sxs-lookup"><span data-stu-id="cfc1b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="cfc1b-136"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc1b-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cfc1b-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cfc1b-137">Library</span></span><br/> | <dl> <span data-ttu-id="cfc1b-138"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfc1b-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc1b-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfc1b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc1b-140">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="cfc1b-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="cfc1b-141">**Интерфейс Исамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="cfc1b-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




