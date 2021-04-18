---
description: Функция Екуалпинс проверяет, находятся ли два контакта на одном объекте.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Функция Екуалпинс (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685197"
---
# <a name="equalpins-function"></a><span data-ttu-id="360f7-103">Функция Екуалпинс</span><span class="sxs-lookup"><span data-stu-id="360f7-103">EqualPins function</span></span>

<span data-ttu-id="360f7-104">Функция Екуалпинс проверяет, находятся ли два контакта на одном объекте.</span><span class="sxs-lookup"><span data-stu-id="360f7-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="360f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="360f7-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="360f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="360f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360f7-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="360f7-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="360f7-108">Указатель на один ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="360f7-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="360f7-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="360f7-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="360f7-110">Указатель на другой ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="360f7-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360f7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="360f7-111">Return value</span></span>

<span data-ttu-id="360f7-112">Возвращает **значение true** , если оба контакта находятся в одном объекте, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="360f7-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="360f7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="360f7-113">Requirements</span></span>



| <span data-ttu-id="360f7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="360f7-114">Requirement</span></span> | <span data-ttu-id="360f7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="360f7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360f7-116">Header</span><span class="sxs-lookup"><span data-stu-id="360f7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="360f7-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="360f7-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="360f7-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="360f7-118">Library</span></span><br/> | <dl> <span data-ttu-id="360f7-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="360f7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="360f7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="360f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360f7-121">Различные вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="360f7-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




