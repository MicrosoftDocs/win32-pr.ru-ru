---
description: Метод Сетонешот указывает, будет ли остановлен образец фильтра захвата после того, как фильтр получит пример.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Метод Исамплеграббер:: Сетонешот (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675413"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="05de4-103">Метод Исамплеграббер:: Сетонешот</span><span class="sxs-lookup"><span data-stu-id="05de4-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="05de4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="05de4-104">\[Deprecated.</span></span> <span data-ttu-id="05de4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05de4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05de4-106">Метод **сетонешот** указывает, будет ли остановлен [**образец фильтра захвата**](sample-grabber-filter.md) после того, как фильтр получит пример.</span><span class="sxs-lookup"><span data-stu-id="05de4-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="05de4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05de4-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="05de4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05de4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05de4-109">*онешот*</span><span class="sxs-lookup"><span data-stu-id="05de4-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="05de4-110">Логическое значение, указывающее, будет ли остановлен образец фильтра захвата после получения образца.</span><span class="sxs-lookup"><span data-stu-id="05de4-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="05de4-111">Значение</span><span class="sxs-lookup"><span data-stu-id="05de4-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="05de4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="05de4-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="05de4-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="05de4-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="05de4-114">Пример захвата останавливается после первой выборки.</span><span class="sxs-lookup"><span data-stu-id="05de4-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="05de4-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="05de4-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="05de4-116">После первой выборки образец захвата продолжит обрабатывать образцы.</span><span class="sxs-lookup"><span data-stu-id="05de4-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="05de4-117">Это поведение установлено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05de4-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05de4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05de4-118">Return value</span></span>

<span data-ttu-id="05de4-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="05de4-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05de4-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05de4-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05de4-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05de4-121">Remarks</span></span>

<span data-ttu-id="05de4-122">Используйте этот метод, чтобы получить один пример из потока следующим образом:</span><span class="sxs-lookup"><span data-stu-id="05de4-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="05de4-123">Вызовите **сетонешот** со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="05de4-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="05de4-124">При необходимости используйте интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , чтобы перейти к положению в потоке.</span><span class="sxs-lookup"><span data-stu-id="05de4-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="05de4-125">Вызовите [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , чтобы запустить граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="05de4-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="05de4-126">Вызовите метод [**имедиаевент:: ваитфоркомплетион**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) , чтобы дождаться остановки графа.</span><span class="sxs-lookup"><span data-stu-id="05de4-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="05de4-127">Кроме того, можно вызвать [**имедиаевент:: четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) , чтобы получить события графа, пока не появится событие [**\_ завершения EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="05de4-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="05de4-128">После остановки захвата образца граф фильтра по-прежнему находится в состоянии выполняется.</span><span class="sxs-lookup"><span data-stu-id="05de4-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="05de4-129">Чтобы получить другой пример, можно найти или приостановить граф.</span><span class="sxs-lookup"><span data-stu-id="05de4-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="05de4-130">В более ранней версии документации указано, что граф фильтра останавливается после получения образца.</span><span class="sxs-lookup"><span data-stu-id="05de4-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="05de4-131">Это неточно.</span><span class="sxs-lookup"><span data-stu-id="05de4-131">That is not accurate.</span></span> <span data-ttu-id="05de4-132">Поток завершается, но граф остается в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="05de4-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="05de4-133">Образец захвата реализует Однофакторный режим, вызывая [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) в подчиненном фильтре и возвращая \_ false из метода [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="05de4-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="05de4-134">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="05de4-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05de4-135">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="05de4-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05de4-136">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="05de4-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05de4-137">Требования</span><span class="sxs-lookup"><span data-stu-id="05de4-137">Requirements</span></span>



| <span data-ttu-id="05de4-138">Требование</span><span class="sxs-lookup"><span data-stu-id="05de4-138">Requirement</span></span> | <span data-ttu-id="05de4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="05de4-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05de4-140">Header</span><span class="sxs-lookup"><span data-stu-id="05de4-140">Header</span></span><br/>  | <dl> <span data-ttu-id="05de4-141"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="05de4-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05de4-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05de4-142">Library</span></span><br/> | <dl> <span data-ttu-id="05de4-143"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05de4-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05de4-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05de4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05de4-145">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="05de4-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="05de4-146">**Интерфейс Исамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="05de4-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




