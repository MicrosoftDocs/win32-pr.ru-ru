---
description: '\_Переменная-член m паллок является указателем на интерфейс имемаллокатор распределителя памяти.'
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Элемент Кпуллпин:: m_pAlloc (Пуллпин. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669053"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="33953-103">Элемент Кпуллпин:: m \_ паллок</span><span class="sxs-lookup"><span data-stu-id="33953-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="33953-104">`m_pAlloc`Переменная-член является указателем на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя памяти.</span><span class="sxs-lookup"><span data-stu-id="33953-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="33953-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33953-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="33953-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="33953-106">Remarks</span></span>

<span data-ttu-id="33953-107">Метод [**кпуллпин::D еЦидеаллокатор**](cpullpin-decideallocator.md) задает эту переменную члена.</span><span class="sxs-lookup"><span data-stu-id="33953-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="33953-108">Требования</span><span class="sxs-lookup"><span data-stu-id="33953-108">Requirements</span></span>



| <span data-ttu-id="33953-109">Требование</span><span class="sxs-lookup"><span data-stu-id="33953-109">Requirement</span></span> | <span data-ttu-id="33953-110">Значение</span><span class="sxs-lookup"><span data-stu-id="33953-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33953-111">Header</span><span class="sxs-lookup"><span data-stu-id="33953-111">Header</span></span><br/>  | <dl> <span data-ttu-id="33953-112"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="33953-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="33953-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33953-113">Library</span></span><br/> | <dl> <span data-ttu-id="33953-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="33953-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33953-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33953-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33953-116">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="33953-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




