---
description: Метод конструктора Кдисппарамс. Кдисппарамс.
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
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095792"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="27ccf-103">Кдисппарамс. Кдисппарамс, конструктор</span><span class="sxs-lookup"><span data-stu-id="27ccf-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="27ccf-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="27ccf-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27ccf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27ccf-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="27ccf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27ccf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27ccf-107">*наргс*</span><span class="sxs-lookup"><span data-stu-id="27ccf-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="27ccf-108">Количество аргументов, переданных методу или свойству.</span><span class="sxs-lookup"><span data-stu-id="27ccf-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="27ccf-109">*паргс*</span><span class="sxs-lookup"><span data-stu-id="27ccf-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="27ccf-110">Указатель на список аргументов.</span><span class="sxs-lookup"><span data-stu-id="27ccf-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="27ccf-111">В списке каждый аргумент сохраняется с типом Variant.</span><span class="sxs-lookup"><span data-stu-id="27ccf-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27ccf-112">Требования</span><span class="sxs-lookup"><span data-stu-id="27ccf-112">Requirements</span></span>



| <span data-ttu-id="27ccf-113">Требование</span><span class="sxs-lookup"><span data-stu-id="27ccf-113">Requirement</span></span> | <span data-ttu-id="27ccf-114">Значение</span><span class="sxs-lookup"><span data-stu-id="27ccf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27ccf-115">Header</span><span class="sxs-lookup"><span data-stu-id="27ccf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="27ccf-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27ccf-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="27ccf-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27ccf-117">Library</span></span><br/> | <dl> <span data-ttu-id="27ccf-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="27ccf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27ccf-119">См. также</span><span class="sxs-lookup"><span data-stu-id="27ccf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ccf-120">**Класс Кдисппарамс**</span><span class="sxs-lookup"><span data-stu-id="27ccf-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




