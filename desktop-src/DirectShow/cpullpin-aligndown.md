---
description: Метод Алигндовн усекает значение до указанной границы выравнивания.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Кпуллпин. Алигндовн, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675591"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="a233f-103">Кпуллпин. Алигндовн, метод</span><span class="sxs-lookup"><span data-stu-id="a233f-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="a233f-104">`AlignDown`Метод усекает значение до указанной границы выравнивания.</span><span class="sxs-lookup"><span data-stu-id="a233f-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="a233f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a233f-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="a233f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a233f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a233f-107">*залив*</span><span class="sxs-lookup"><span data-stu-id="a233f-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="a233f-108">Указывает число для выровняйте.</span><span class="sxs-lookup"><span data-stu-id="a233f-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="a233f-109">*лалигн*</span><span class="sxs-lookup"><span data-stu-id="a233f-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="a233f-110">Задает границу выравнивания.</span><span class="sxs-lookup"><span data-stu-id="a233f-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a233f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a233f-111">Return value</span></span>

<span data-ttu-id="a233f-112">Возвращает согласованный результат.</span><span class="sxs-lookup"><span data-stu-id="a233f-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="a233f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a233f-113">Requirements</span></span>



| <span data-ttu-id="a233f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a233f-114">Requirement</span></span> | <span data-ttu-id="a233f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a233f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a233f-116">Header</span><span class="sxs-lookup"><span data-stu-id="a233f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a233f-117"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="a233f-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a233f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a233f-118">Library</span></span><br/> | <dl> <span data-ttu-id="a233f-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a233f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a233f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a233f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a233f-121">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="a233f-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




