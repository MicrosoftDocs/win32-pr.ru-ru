---
description: Метод Get \_ mediaType возвращает текущий тип выходного носителя фильтра.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Метод Иресизе:: get_MediaType (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679838"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="933b8-103">Метод Иресизе:: Get \_ mediaType</span><span class="sxs-lookup"><span data-stu-id="933b8-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="933b8-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="933b8-104">\[Deprecated.</span></span> <span data-ttu-id="933b8-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="933b8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="933b8-106">`get_MediaType`Метод возвращает текущий тип выходного носителя фильтра.</span><span class="sxs-lookup"><span data-stu-id="933b8-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="933b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="933b8-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="933b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="933b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933b8-109">*платежная плата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="933b8-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="933b8-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , выделенную вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="933b8-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="933b8-111">Метод заполняет эту структуру типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="933b8-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="933b8-112">Вызывающий объект должен освободить блок формата, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="933b8-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933b8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="933b8-113">Return value</span></span>

<span data-ttu-id="933b8-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="933b8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="933b8-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="933b8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="933b8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="933b8-116">Remarks</span></span>

<span data-ttu-id="933b8-117">Если тип выходного носителя не задан, возвращается тип носителя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="933b8-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="933b8-118">Фильтр должен обновить тип выходного носителя, когда вызываются методы **размещения \_ mediaType** или Where **\_ size** ; тип носителя, возвращаемый методом, `get_MediaType` должен отражать эти изменения.</span><span class="sxs-lookup"><span data-stu-id="933b8-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="933b8-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="933b8-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="933b8-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="933b8-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="933b8-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="933b8-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="933b8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="933b8-122">Requirements</span></span>



| <span data-ttu-id="933b8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="933b8-123">Requirement</span></span> | <span data-ttu-id="933b8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="933b8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="933b8-125">Версия</span><span class="sxs-lookup"><span data-stu-id="933b8-125">Version</span></span><br/> | <span data-ttu-id="933b8-126">DirectX 9,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="933b8-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="933b8-127">Header</span><span class="sxs-lookup"><span data-stu-id="933b8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="933b8-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="933b8-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="933b8-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="933b8-129">Library</span></span><br/> | <dl> <span data-ttu-id="933b8-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="933b8-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933b8-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="933b8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933b8-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="933b8-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="933b8-133">**Интерфейс Иресизе**</span><span class="sxs-lookup"><span data-stu-id="933b8-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




