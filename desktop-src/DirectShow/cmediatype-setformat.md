---
description: Метод Сетформат инициализирует блок формата.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Кмедиатипе. Сетформат, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675796"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="747a7-103">Кмедиатипе. Сетформат, метод</span><span class="sxs-lookup"><span data-stu-id="747a7-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="747a7-104">`SetFormat`Метод инициализирует блок формата.</span><span class="sxs-lookup"><span data-stu-id="747a7-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="747a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="747a7-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="747a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="747a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747a7-107">*пформат*</span><span class="sxs-lookup"><span data-stu-id="747a7-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="747a7-108">Указатель на блок памяти, который содержит блок формата.</span><span class="sxs-lookup"><span data-stu-id="747a7-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="747a7-109">*length*</span><span class="sxs-lookup"><span data-stu-id="747a7-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="747a7-110">Длина блока формата в байтах.</span><span class="sxs-lookup"><span data-stu-id="747a7-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747a7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="747a7-111">Return value</span></span>

<span data-ttu-id="747a7-112">Возвращает **значение true** в случае успеха или **значение false** , если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="747a7-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="747a7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="747a7-113">Remarks</span></span>

<span data-ttu-id="747a7-114">Этот метод выделяет память для блока формата и копирует буфер, указанный параметром *пформат* , в новый блок формата.</span><span class="sxs-lookup"><span data-stu-id="747a7-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="747a7-115">Если тип мультимедиа уже содержит блок формата, старый он освобождается.</span><span class="sxs-lookup"><span data-stu-id="747a7-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="747a7-116">Метод также задает элемент **кбформат** структуры **\_ \_ типа мультимедиа AM** .</span><span class="sxs-lookup"><span data-stu-id="747a7-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="747a7-117">Чтобы задать тип формата, вызовите метод [**кмедиатипе:: сетформаттипе**](cmediatype-setformattype.md) .</span><span class="sxs-lookup"><span data-stu-id="747a7-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="747a7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="747a7-118">Requirements</span></span>



| <span data-ttu-id="747a7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="747a7-119">Requirement</span></span> | <span data-ttu-id="747a7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="747a7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="747a7-121">Header</span><span class="sxs-lookup"><span data-stu-id="747a7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="747a7-122"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="747a7-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="747a7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="747a7-123">Library</span></span><br/> | <dl> <span data-ttu-id="747a7-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="747a7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747a7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="747a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747a7-126">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="747a7-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




