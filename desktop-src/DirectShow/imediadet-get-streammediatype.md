---
description: Метод Get \_ стреаммедиатипе Извлекает тип носителя текущего потока. Все видеопотоки преобразуются в типы ВИДЕОИНФОХЕАДЕР, а все звуковые потоки преобразуются в типы ВАВЕФОРМАТЕКС.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'Метод Имедиадет:: get_StreamMediaType (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679708"
---
# <a name="imediadetget_streammediatype-method"></a><span data-ttu-id="72efd-104">Метод Имедиадет:: Get \_ стреаммедиатипе</span><span class="sxs-lookup"><span data-stu-id="72efd-104">IMediaDet::get\_StreamMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="72efd-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="72efd-105">\[Deprecated.</span></span> <span data-ttu-id="72efd-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72efd-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72efd-107">`get_StreamMediaType`Метод извлекает тип носителя текущего потока.</span><span class="sxs-lookup"><span data-stu-id="72efd-107">The `get_StreamMediaType` method retrieves the media type of the current stream.</span></span> <span data-ttu-id="72efd-108">Все видеопотоки преобразуются в типы [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , а все звуковые потоки преобразуются в типы [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="72efd-108">All video streams are converted to [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) types, and all audio streams are converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) types.</span></span>

## <a name="syntax"></a><span data-ttu-id="72efd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72efd-109">Syntax</span></span>


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="72efd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="72efd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72efd-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="72efd-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="72efd-112">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , которая заполнена типом носителя.</span><span class="sxs-lookup"><span data-stu-id="72efd-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72efd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72efd-113">Return value</span></span>

<span data-ttu-id="72efd-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="72efd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72efd-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72efd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72efd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72efd-116">Remarks</span></span>

<span data-ttu-id="72efd-117">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-117">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="72efd-118">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="72efd-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="72efd-119">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="72efd-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="72efd-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72efd-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72efd-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72efd-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="72efd-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72efd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="72efd-123">Requirements</span></span>



| <span data-ttu-id="72efd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="72efd-124">Requirement</span></span> | <span data-ttu-id="72efd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="72efd-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72efd-126">Header</span><span class="sxs-lookup"><span data-stu-id="72efd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="72efd-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="72efd-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72efd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72efd-128">Library</span></span><br/> | <dl> <span data-ttu-id="72efd-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72efd-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72efd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72efd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72efd-131">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="72efd-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="72efd-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="72efd-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
