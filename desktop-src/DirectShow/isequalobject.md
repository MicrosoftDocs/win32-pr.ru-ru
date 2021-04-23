---
description: Функция Исекуалобжект проверяет, находятся ли два интерфейса в одном объекте.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Функция Исекуалобжект (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685295"
---
# <a name="isequalobject-function"></a><span data-ttu-id="0d642-103">Функция Исекуалобжект</span><span class="sxs-lookup"><span data-stu-id="0d642-103">IsEqualObject function</span></span>

<span data-ttu-id="0d642-104">`IsEqualObject`Функция проверяет, находятся ли два интерфейса на одном объекте.</span><span class="sxs-lookup"><span data-stu-id="0d642-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d642-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d642-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="0d642-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d642-107">*пфирст*</span><span class="sxs-lookup"><span data-stu-id="0d642-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="0d642-108">Указатель на один интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0d642-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="0d642-109">*псеконд*</span><span class="sxs-lookup"><span data-stu-id="0d642-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="0d642-110">Указатель на другой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0d642-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d642-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d642-111">Return value</span></span>

<span data-ttu-id="0d642-112">Возвращает **значение true** , если интерфейсы находятся в одном объекте, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0d642-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d642-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0d642-113">Requirements</span></span>



| <span data-ttu-id="0d642-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0d642-114">Requirement</span></span> | <span data-ttu-id="0d642-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0d642-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d642-116">Header</span><span class="sxs-lookup"><span data-stu-id="0d642-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0d642-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d642-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0d642-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d642-118">Library</span></span><br/> | <dl> <span data-ttu-id="0d642-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0d642-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d642-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d642-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d642-121">Различные вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="0d642-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




