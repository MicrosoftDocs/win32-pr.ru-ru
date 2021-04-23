---
description: Метод Жетмедиатипе извлекает несжатый тип носителя для группы.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'Метод Иамтимелинеграуп:: Жетмедиатипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680065"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="53eb5-103">Метод Иамтимелинеграуп:: Жетмедиатипе</span><span class="sxs-lookup"><span data-stu-id="53eb5-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="53eb5-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="53eb5-104">\[Deprecated.</span></span> <span data-ttu-id="53eb5-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53eb5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53eb5-106">`GetMediaType`Метод извлекает несжатый тип носителя для группы.</span><span class="sxs-lookup"><span data-stu-id="53eb5-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="53eb5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53eb5-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="53eb5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53eb5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53eb5-109">*платежная плата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53eb5-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53eb5-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , которая заполнена типом носителя.</span><span class="sxs-lookup"><span data-stu-id="53eb5-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53eb5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53eb5-111">Return value</span></span>

<span data-ttu-id="53eb5-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="53eb5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53eb5-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53eb5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53eb5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53eb5-114">Remarks</span></span>

<span data-ttu-id="53eb5-115">Вызывающий объект должен освободить блок формата возвращаемого типа мультимедиа, заданный в элементе **пбформат** возвращаемой \_ \_ структуры типа данных AM.</span><span class="sxs-lookup"><span data-stu-id="53eb5-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="53eb5-116">Можно использовать вспомогательную функцию [**фримедиатипе**](freemediatype.md) из библиотеки базовых классов.</span><span class="sxs-lookup"><span data-stu-id="53eb5-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="53eb5-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="53eb5-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53eb5-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53eb5-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53eb5-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="53eb5-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53eb5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="53eb5-120">Requirements</span></span>



| <span data-ttu-id="53eb5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="53eb5-121">Requirement</span></span> | <span data-ttu-id="53eb5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="53eb5-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53eb5-123">Header</span><span class="sxs-lookup"><span data-stu-id="53eb5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="53eb5-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="53eb5-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53eb5-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53eb5-125">Library</span></span><br/> | <dl> <span data-ttu-id="53eb5-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53eb5-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53eb5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53eb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53eb5-128">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="53eb5-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="53eb5-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="53eb5-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




