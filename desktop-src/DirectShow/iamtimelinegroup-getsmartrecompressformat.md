---
description: Метод Жетсмартрекомпрессформат извлекает текущий формат сжатия для интеллектуального повторного сжатия.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Метод Иамтимелинеграуп:: Жетсмартрекомпрессформат (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688907"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="a90f5-103">Метод Иамтимелинеграуп:: Жетсмартрекомпрессформат</span><span class="sxs-lookup"><span data-stu-id="a90f5-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="a90f5-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a90f5-104">\[Deprecated.</span></span> <span data-ttu-id="a90f5-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a90f5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a90f5-106">`GetSmartRecompressFormat`Метод получает текущий формат сжатия для интеллектуального повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="a90f5-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90f5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a90f5-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a90f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a90f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90f5-109">*ппформат*</span><span class="sxs-lookup"><span data-stu-id="a90f5-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a90f5-110">Получает указатель на структуру [**SCompFmt0**](scompfmt0.md) , приводится как указатель на тип long.</span><span class="sxs-lookup"><span data-stu-id="a90f5-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="a90f5-111">Если метод завершается с ошибкой, ему присваивается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a90f5-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90f5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a90f5-112">Return value</span></span>

<span data-ttu-id="a90f5-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a90f5-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a90f5-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a90f5-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a90f5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a90f5-115">Remarks</span></span>

<span data-ttu-id="a90f5-116">Если в приложении не задан формат интеллектуального сжатия (путем вызова [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md)), то формат, возвращаемый этим методом, будет недопустимым.</span><span class="sxs-lookup"><span data-stu-id="a90f5-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="a90f5-117">Вызовите метод [**иамтимелинеграуп:: иссмартрекомпрессформатсет**](iamtimelinegroup-issmartrecompressformatset.md) , чтобы определить, был ли задан формат сжатия.</span><span class="sxs-lookup"><span data-stu-id="a90f5-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="a90f5-118">Если метод завершился с ошибкой, вызывающий объект должен освободить возвращенный тип мультимедиа и удалить структуру [**SCompFmt0**](scompfmt0.md) :</span><span class="sxs-lookup"><span data-stu-id="a90f5-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="a90f5-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a90f5-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a90f5-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a90f5-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a90f5-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a90f5-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a90f5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a90f5-122">Requirements</span></span>



| <span data-ttu-id="a90f5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a90f5-123">Requirement</span></span> | <span data-ttu-id="a90f5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a90f5-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a90f5-125">Header</span><span class="sxs-lookup"><span data-stu-id="a90f5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a90f5-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a90f5-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a90f5-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a90f5-127">Library</span></span><br/> | <dl> <span data-ttu-id="a90f5-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a90f5-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a90f5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a90f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90f5-130">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="a90f5-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="a90f5-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a90f5-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




