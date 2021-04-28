---
description: Конструктор Кмедиатипе. Кмедиатипе (Мтипе. h) — метод-конструктор.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметры кмтипе и фр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095422"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="50ffa-103">Конструктор Кмедиатипе. Кмедиатипе (Мтипе. h)</span><span class="sxs-lookup"><span data-stu-id="50ffa-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="50ffa-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="50ffa-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ffa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50ffa-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="50ffa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50ffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50ffa-107">*кмтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="50ffa-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="50ffa-108">Ссылка на `CMediaType` объект.</span><span class="sxs-lookup"><span data-stu-id="50ffa-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="50ffa-109">Конструктор копирует тип мультимедиа в новый объект, включая блок формата, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="50ffa-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="50ffa-110">*фр*</span><span class="sxs-lookup"><span data-stu-id="50ffa-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="50ffa-111">Указатель на переменную, которая получает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="50ffa-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="50ffa-112">Этот параметр может быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="50ffa-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="50ffa-113">В противном случае перед вызовом конструктора вызывающий объект должен установить значение, равное « \_ ОК».</span><span class="sxs-lookup"><span data-stu-id="50ffa-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="50ffa-114">Если конструктор завершается неудачно, ему присваивается значение кода сбоя.</span><span class="sxs-lookup"><span data-stu-id="50ffa-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50ffa-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="50ffa-115">Remarks</span></span>

<span data-ttu-id="50ffa-116">Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="50ffa-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ffa-117">Требования</span><span class="sxs-lookup"><span data-stu-id="50ffa-117">Requirements</span></span>



| <span data-ttu-id="50ffa-118">Требование</span><span class="sxs-lookup"><span data-stu-id="50ffa-118">Requirement</span></span> | <span data-ttu-id="50ffa-119">Значение</span><span class="sxs-lookup"><span data-stu-id="50ffa-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ffa-120">Header</span><span class="sxs-lookup"><span data-stu-id="50ffa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="50ffa-121"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50ffa-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="50ffa-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50ffa-122">Library</span></span><br/> | <dl> <span data-ttu-id="50ffa-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="50ffa-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ffa-124">См. также</span><span class="sxs-lookup"><span data-stu-id="50ffa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ffa-125">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="50ffa-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




