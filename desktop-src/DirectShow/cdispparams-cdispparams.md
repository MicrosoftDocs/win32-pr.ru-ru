---
description: Метод конструктора.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Конструктор Кдисппарамс. Кдисппарамс (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675812"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="50830-103">Кдисппарамс. Кдисппарамс, конструктор</span><span class="sxs-lookup"><span data-stu-id="50830-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="50830-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="50830-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="50830-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50830-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="50830-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50830-107">*наргс*</span><span class="sxs-lookup"><span data-stu-id="50830-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="50830-108">Количество аргументов, переданных методу или свойству.</span><span class="sxs-lookup"><span data-stu-id="50830-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="50830-109">*паргс*</span><span class="sxs-lookup"><span data-stu-id="50830-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="50830-110">Указатель на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="50830-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="50830-111">В списке каждый аргумент сохраняется с типом Variant.</span><span class="sxs-lookup"><span data-stu-id="50830-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50830-112">Требования</span><span class="sxs-lookup"><span data-stu-id="50830-112">Requirements</span></span>



| <span data-ttu-id="50830-113">Требование</span><span class="sxs-lookup"><span data-stu-id="50830-113">Requirement</span></span> | <span data-ttu-id="50830-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50830-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50830-115">Header</span><span class="sxs-lookup"><span data-stu-id="50830-115">Header</span></span><br/>  | <dl> <span data-ttu-id="50830-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50830-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50830-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50830-117">Library</span></span><br/> | <dl> <span data-ttu-id="50830-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="50830-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50830-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50830-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50830-120">**Класс Кдисппарамс**</span><span class="sxs-lookup"><span data-stu-id="50830-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




