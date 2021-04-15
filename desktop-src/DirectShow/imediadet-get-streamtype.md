---
description: Метод Get \_ стреамтипе извлекает глобальный уникальный идентификатор (GUID) для типа мультимедиа текущего потока.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Метод Имедиадет:: get_StreamType (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689259"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="2669f-103">Метод Имедиадет:: Get \_ стреамтипе</span><span class="sxs-lookup"><span data-stu-id="2669f-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="2669f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2669f-104">\[Deprecated.</span></span> <span data-ttu-id="2669f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2669f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2669f-106">`get_StreamType`Метод получает Глобальный уникальный идентификатор (GUID) для типа мультимедиа текущего потока.</span><span class="sxs-lookup"><span data-stu-id="2669f-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="2669f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2669f-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2669f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2669f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2669f-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2669f-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2669f-110">Получает основной GUID типа для типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2669f-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2669f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2669f-111">Return value</span></span>

<span data-ttu-id="2669f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2669f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2669f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2669f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2669f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2669f-114">Remarks</span></span>

<span data-ttu-id="2669f-115">Этот метод извлекает элемент **мажортипе** структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="2669f-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="2669f-116">Структура **\_ \_ типа мультимедиа AM** описывает формат потока, а элемент **мажортипе** — идентификатор GUID, указывающий общую категорию, например аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="2669f-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="2669f-117">Для потока видео GUID — это видео типа MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="2669f-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="2669f-118">Для звукового сигнала используется параметр MEDIATYPE \_ Audio.</span><span class="sxs-lookup"><span data-stu-id="2669f-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="2669f-119">Чтобы получить всю структуру **\_ \_ типа мультимедиа AM** , вызовите метод [**имедиадет:: Get \_ стреаммедиатипе**](imediadet-get-streammediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="2669f-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="2669f-120">Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="2669f-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="2669f-121">Если средство обнаружения мультимедиа находится в режиме захвата растрового изображения, этот метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="2669f-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="2669f-122">Дополнительные сведения см. в разделе [**имедиадет:: ентербитмапграбмоде**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="2669f-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="2669f-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2669f-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2669f-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2669f-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2669f-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2669f-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2669f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2669f-126">Requirements</span></span>



| <span data-ttu-id="2669f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2669f-127">Requirement</span></span> | <span data-ttu-id="2669f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2669f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2669f-129">Header</span><span class="sxs-lookup"><span data-stu-id="2669f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2669f-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2669f-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2669f-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2669f-131">Library</span></span><br/> | <dl> <span data-ttu-id="2669f-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2669f-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2669f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2669f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2669f-134">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="2669f-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="2669f-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2669f-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




