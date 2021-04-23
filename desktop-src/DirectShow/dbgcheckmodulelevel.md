---
description: Функция Дбгчеккмодулелевел проверяет, включено ли ведение журнала для заданных типов сообщений и уровня. Игнорируется в розничных сборках.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Функция Дбгчеккмодулелевел (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679869"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="fa7c6-104">Функция Дбгчеккмодулелевел</span><span class="sxs-lookup"><span data-stu-id="fa7c6-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="fa7c6-105">`DbgCheckModuleLevel`Функция проверяет, включено ли ведение журнала для заданных типов сообщений и уровня.</span><span class="sxs-lookup"><span data-stu-id="fa7c6-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="fa7c6-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="fa7c6-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7c6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa7c6-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="fa7c6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa7c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7c6-109">*Типы*</span><span class="sxs-lookup"><span data-stu-id="fa7c6-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="fa7c6-110">Побитовое сочетание одного или нескольких типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa7c6-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="fa7c6-111">*Уровень*</span><span class="sxs-lookup"><span data-stu-id="fa7c6-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="fa7c6-112">Уровень ведения журнала</span><span class="sxs-lookup"><span data-stu-id="fa7c6-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7c6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa7c6-113">Return value</span></span>

<span data-ttu-id="fa7c6-114">Возвращает **значение true** , если ведение журнала для любого из указанных типов сообщений установлено на указанный уровень или выше.</span><span class="sxs-lookup"><span data-stu-id="fa7c6-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="fa7c6-115">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fa7c6-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7c6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fa7c6-116">Requirements</span></span>



| <span data-ttu-id="fa7c6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fa7c6-117">Requirement</span></span> | <span data-ttu-id="fa7c6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fa7c6-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7c6-119">Header</span><span class="sxs-lookup"><span data-stu-id="fa7c6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fa7c6-120"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa7c6-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa7c6-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa7c6-121">Library</span></span><br/> | <dl> <span data-ttu-id="fa7c6-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fa7c6-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa7c6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa7c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7c6-124">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="fa7c6-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




