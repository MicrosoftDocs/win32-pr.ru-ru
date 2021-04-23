---
description: Метод Алигнуп Округляет значение до указанной границы выравнивания. Примечание удалено в Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Кпуллпин. Алигнуп, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675590"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="c2330-104">Кпуллпин. Алигнуп, метод</span><span class="sxs-lookup"><span data-stu-id="c2330-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="c2330-105">Метод **алигнуп** Округляет значение до указанной границы выравнивания.</span><span class="sxs-lookup"><span data-stu-id="c2330-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="c2330-106">Удалено в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c2330-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c2330-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2330-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="c2330-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2330-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2330-109">*залив*</span><span class="sxs-lookup"><span data-stu-id="c2330-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="c2330-110">Указывает число для выровняйте.</span><span class="sxs-lookup"><span data-stu-id="c2330-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="c2330-111">*лалигн*</span><span class="sxs-lookup"><span data-stu-id="c2330-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="c2330-112">Задает границу выравнивания.</span><span class="sxs-lookup"><span data-stu-id="c2330-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2330-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2330-113">Return value</span></span>

<span data-ttu-id="c2330-114">Возвращает согласованный результат.</span><span class="sxs-lookup"><span data-stu-id="c2330-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2330-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2330-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c2330-116">Этот метод может привести к числу переполнений, если *все* + (*лалигн* -1) переполнены.</span><span class="sxs-lookup"><span data-stu-id="c2330-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2330-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c2330-117">Requirements</span></span>



| <span data-ttu-id="c2330-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c2330-118">Requirement</span></span> | <span data-ttu-id="c2330-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c2330-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2330-120">Header</span><span class="sxs-lookup"><span data-stu-id="c2330-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c2330-121"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2330-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c2330-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2330-122">Library</span></span><br/> | <dl> <span data-ttu-id="c2330-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c2330-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2330-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2330-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2330-125">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="c2330-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




