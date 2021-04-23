---
description: Функция Дбгсетмодулелевел задает уровень ведения журнала для одного или нескольких типов сообщений. Игнорируется в розничных сборках.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Функция Дбгсетмодулелевел (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657221"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="e9b68-104">Функция Дбгсетмодулелевел</span><span class="sxs-lookup"><span data-stu-id="e9b68-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="e9b68-105">Функция **дбгсетмодулелевел** задает уровень ведения журнала для одного или нескольких типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9b68-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="e9b68-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="e9b68-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b68-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9b68-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="e9b68-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9b68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b68-109">*Типы*</span><span class="sxs-lookup"><span data-stu-id="e9b68-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b68-110">Побитовое сочетание одного или нескольких типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9b68-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="e9b68-111">*Уровень*</span><span class="sxs-lookup"><span data-stu-id="e9b68-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b68-112">Уровень ведения журнала для указанных типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e9b68-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b68-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9b68-113">Return value</span></span>

<span data-ttu-id="e9b68-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e9b68-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b68-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e9b68-115">Requirements</span></span>



| <span data-ttu-id="e9b68-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e9b68-116">Requirement</span></span> | <span data-ttu-id="e9b68-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e9b68-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b68-118">Header</span><span class="sxs-lookup"><span data-stu-id="e9b68-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e9b68-119"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9b68-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9b68-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9b68-120">Library</span></span><br/> | <dl> <span data-ttu-id="e9b68-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e9b68-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b68-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9b68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b68-123">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="e9b68-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




