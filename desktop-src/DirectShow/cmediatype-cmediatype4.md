---
description: Метод конструктора.
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
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389068"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="8a4b2-103">Конструктор Кмедиатипе. Кмедиатипе (Мтипе. h)</span><span class="sxs-lookup"><span data-stu-id="8a4b2-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="8a4b2-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a4b2-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="8a4b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a4b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a4b2-107">*кмтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="8a4b2-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4b2-108">Ссылка на `CMediaType` объект.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="8a4b2-109">Конструктор копирует тип мультимедиа в новый объект, включая блок формата, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="8a4b2-110">*фр*</span><span class="sxs-lookup"><span data-stu-id="8a4b2-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8a4b2-111">Указатель на переменную, которая получает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="8a4b2-112">Этот параметр может быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="8a4b2-113">В противном случае перед вызовом конструктора вызывающий объект должен установить значение, равное « \_ ОК».</span><span class="sxs-lookup"><span data-stu-id="8a4b2-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="8a4b2-114">Если конструктор завершается неудачно, ему присваивается значение кода сбоя.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a4b2-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="8a4b2-115">Remarks</span></span>

<span data-ttu-id="8a4b2-116">Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a4b2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8a4b2-117">Requirements</span></span>



| <span data-ttu-id="8a4b2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8a4b2-118">Requirement</span></span> | <span data-ttu-id="8a4b2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8a4b2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4b2-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8a4b2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8a4b2-121"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a4b2-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8a4b2-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a4b2-122">Library</span></span><br/> | <dl> <span data-ttu-id="8a4b2-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8a4b2-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a4b2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8a4b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4b2-125">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




