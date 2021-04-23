---
description: Метод конструктора.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Конструктор Ценуммедиатипес. Ценуммедиатипес (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657591"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="388ee-103">Ценуммедиатипес. Ценуммедиатипес, конструктор</span><span class="sxs-lookup"><span data-stu-id="388ee-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="388ee-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="388ee-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="388ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="388ee-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="388ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="388ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="388ee-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="388ee-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="388ee-108">Указатель на ПИН-код, на котором должно быть выполнено перечисление.</span><span class="sxs-lookup"><span data-stu-id="388ee-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="388ee-109">*пенуммедиатипес*</span><span class="sxs-lookup"><span data-stu-id="388ee-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="388ee-110">Указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) перечислителя, который необходимо клонировать, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="388ee-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="388ee-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="388ee-111">Remarks</span></span>

<span data-ttu-id="388ee-112">Если *пенуммедиатипес* имеет **значение NULL**, этот метод инициализирует перечислитель до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="388ee-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="388ee-113">В противном случае он дублирует внутреннее состояние перечислителя, заданного параметром *пенуммедиатипес*.</span><span class="sxs-lookup"><span data-stu-id="388ee-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="388ee-114">Требования</span><span class="sxs-lookup"><span data-stu-id="388ee-114">Requirements</span></span>



| <span data-ttu-id="388ee-115">Требование</span><span class="sxs-lookup"><span data-stu-id="388ee-115">Requirement</span></span> | <span data-ttu-id="388ee-116">Значение</span><span class="sxs-lookup"><span data-stu-id="388ee-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="388ee-117">Header</span><span class="sxs-lookup"><span data-stu-id="388ee-117">Header</span></span><br/>  | <dl> <span data-ttu-id="388ee-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="388ee-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="388ee-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="388ee-119">Library</span></span><br/> | <dl> <span data-ttu-id="388ee-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="388ee-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388ee-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="388ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388ee-122">**Класс Ценуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="388ee-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




