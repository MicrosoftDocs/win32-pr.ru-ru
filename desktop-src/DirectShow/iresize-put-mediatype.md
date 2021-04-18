---
description: Метод размещения \_ mediaType задает тип выходного носителя для фильтра изменения размера.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'Иресизе: метод ut_MediaType:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675362"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="301eb-103">Иресизе: метод:p UT \_ mediaType</span><span class="sxs-lookup"><span data-stu-id="301eb-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="301eb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="301eb-104">\[Deprecated.</span></span> <span data-ttu-id="301eb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="301eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="301eb-106">`put_MediaType`Метод задает тип выходного носителя для фильтра изменения размера.</span><span class="sxs-lookup"><span data-stu-id="301eb-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="301eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="301eb-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="301eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="301eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301eb-109">*платежная плата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="301eb-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="301eb-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , содержащую тип носителя.</span><span class="sxs-lookup"><span data-stu-id="301eb-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301eb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="301eb-111">Return value</span></span>

<span data-ttu-id="301eb-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="301eb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="301eb-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="301eb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="301eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="301eb-114">Remarks</span></span>

<span data-ttu-id="301eb-115">Алгоритм DES вызывает этот метод перед подключением выходного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="301eb-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="301eb-116">Используйте тип носителя в качестве типа носителя выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="301eb-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="301eb-117">Верните этот тип мультимедиа в метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) и проверьте агсинт этот тип в методе [**Ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="301eb-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="301eb-118">DES никогда не вызывает этот метод после подключения выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="301eb-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="301eb-119">В настоящее время DES всегда устанавливает тип выходного носителя в несжатый формат RGB с помощью блока формата **видеоинфохеадер** (тип формата равен Format \_ видеоинфо).</span><span class="sxs-lookup"><span data-stu-id="301eb-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="301eb-120">Подтипом может быть МЕДИАСУБТИПЕ \_ ARGB32, который указывает 32-битный RGB с каналом альфа.</span><span class="sxs-lookup"><span data-stu-id="301eb-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="301eb-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="301eb-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="301eb-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="301eb-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="301eb-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="301eb-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="301eb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="301eb-124">Requirements</span></span>



| <span data-ttu-id="301eb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="301eb-125">Requirement</span></span> | <span data-ttu-id="301eb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="301eb-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="301eb-127">Версия</span><span class="sxs-lookup"><span data-stu-id="301eb-127">Version</span></span><br/> | <span data-ttu-id="301eb-128">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="301eb-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="301eb-129">Header</span><span class="sxs-lookup"><span data-stu-id="301eb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="301eb-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="301eb-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="301eb-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="301eb-131">Library</span></span><br/> | <dl> <span data-ttu-id="301eb-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="301eb-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="301eb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="301eb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301eb-134">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="301eb-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="301eb-135">**Интерфейс Иресизе**</span><span class="sxs-lookup"><span data-stu-id="301eb-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




