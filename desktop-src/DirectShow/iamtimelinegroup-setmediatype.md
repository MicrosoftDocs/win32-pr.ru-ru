---
description: Метод Сетмедиатипе задает несжатый тип носителя для группы.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'Метод Иамтимелинеграуп:: Сетмедиатипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679735"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="2cce5-103">Метод Иамтимелинеграуп:: Сетмедиатипе</span><span class="sxs-lookup"><span data-stu-id="2cce5-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="2cce5-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2cce5-104">\[Deprecated.</span></span> <span data-ttu-id="2cce5-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2cce5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2cce5-106">`SetMediaType`Метод задает несжатый тип носителя для группы.</span><span class="sxs-lookup"><span data-stu-id="2cce5-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cce5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cce5-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2cce5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cce5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cce5-109">*платежная плата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cce5-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cce5-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , описывающую формат.</span><span class="sxs-lookup"><span data-stu-id="2cce5-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cce5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cce5-111">Return value</span></span>

<span data-ttu-id="2cce5-112">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="2cce5-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="2cce5-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2cce5-113">Return code</span></span>                                                                                             | <span data-ttu-id="2cce5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2cce5-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2cce5-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2cce5-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="2cce5-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2cce5-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="2cce5-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2cce5-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="2cce5-118">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="2cce5-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="2cce5-119"><dt>**VFW \_ E \_ инвалидмедиатипе**</dt></span><span class="sxs-lookup"><span data-stu-id="2cce5-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="2cce5-120">Указан недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="2cce5-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2cce5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cce5-121">Remarks</span></span>

<span data-ttu-id="2cce5-122">Поддерживаются следующие типы носителей:</span><span class="sxs-lookup"><span data-stu-id="2cce5-122">The following media types are supported:</span></span>

-   <span data-ttu-id="2cce5-123">Несжатое видео RGB</span><span class="sxs-lookup"><span data-stu-id="2cce5-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="2cce5-124">16 бит на пиксель, формат 555 (МЕДИАСУБТИПЕ \_ RGB555)</span><span class="sxs-lookup"><span data-stu-id="2cce5-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="2cce5-125">24 бита на пиксель (МЕДИАСУБТИПЕ \_ Rgb24)</span><span class="sxs-lookup"><span data-stu-id="2cce5-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="2cce5-126">32 бит на пиксель с альфа (МЕДИАСУБТИПЕ \_ ARGB32, а не медиасубтипе \_ RGB32)</span><span class="sxs-lookup"><span data-stu-id="2cce5-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="2cce5-127">16-разрядный стереозвук PCM (МЕДИАСУБТИПЕ \_ PCM)</span><span class="sxs-lookup"><span data-stu-id="2cce5-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="2cce5-128">Типы видео должны использовать формат \_ видеоинфо для типа формата и [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для блока Format.</span><span class="sxs-lookup"><span data-stu-id="2cce5-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="2cce5-129">Формат [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2cce5-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="2cce5-130">Кроме того, форматы с верхними и видеороликами (*бихеигхт* < 0) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2cce5-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="2cce5-131">Чтобы указать формат сжатия для группы, вызовите метод [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="2cce5-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="2cce5-132">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2cce5-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2cce5-133">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2cce5-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2cce5-134">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2cce5-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cce5-135">Требования</span><span class="sxs-lookup"><span data-stu-id="2cce5-135">Requirements</span></span>



| <span data-ttu-id="2cce5-136">Требование</span><span class="sxs-lookup"><span data-stu-id="2cce5-136">Requirement</span></span> | <span data-ttu-id="2cce5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="2cce5-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cce5-138">Header</span><span class="sxs-lookup"><span data-stu-id="2cce5-138">Header</span></span><br/>  | <dl> <span data-ttu-id="2cce5-139"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cce5-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2cce5-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2cce5-140">Library</span></span><br/> | <dl> <span data-ttu-id="2cce5-141"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cce5-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cce5-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cce5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cce5-143">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="2cce5-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="2cce5-144">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2cce5-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




