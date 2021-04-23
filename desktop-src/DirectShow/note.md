---
description: Макрос примечания отправляет строку в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Примечание (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689336"
---
# <a name="note"></a><span data-ttu-id="2e0cd-104">ПРИМЕЧАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e0cd-104">NOTE</span></span>

<span data-ttu-id="2e0cd-105">`NOTE`Макрос отправляет строку в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="2e0cd-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="2e0cd-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="2e0cd-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="2e0cd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e0cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0cd-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*пформат*</span><span class="sxs-lookup"><span data-stu-id="2e0cd-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="2e0cd-109">Строка формата в стиле printf.</span><span class="sxs-lookup"><span data-stu-id="2e0cd-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="2e0cd-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*—*arg5*</span><span class="sxs-lookup"><span data-stu-id="2e0cd-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="2e0cd-111">Дополнительные аргументы для строки формата.</span><span class="sxs-lookup"><span data-stu-id="2e0cd-111">Additional arguments for the format string.</span></span> <span data-ttu-id="2e0cd-112">Число аргументов должно совпадать с именем макроса.</span><span class="sxs-lookup"><span data-stu-id="2e0cd-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="2e0cd-113">Например, **Note1** принимает один аргумент, а **NOTE5** принимает пять аргументов.</span><span class="sxs-lookup"><span data-stu-id="2e0cd-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e0cd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e0cd-114">Remarks</span></span>

<span data-ttu-id="2e0cd-115">Эти макросы являются вариантами макроса [**дбглог**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0cd-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="2e0cd-116">Они создают сообщения трассировки журнала уровня 5 \_ .</span><span class="sxs-lookup"><span data-stu-id="2e0cd-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="2e0cd-117">Пример</span><span class="sxs-lookup"><span data-stu-id="2e0cd-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="2e0cd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e0cd-118">Requirements</span></span>



| <span data-ttu-id="2e0cd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2e0cd-119">Requirement</span></span> | <span data-ttu-id="2e0cd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2e0cd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0cd-121">Header</span><span class="sxs-lookup"><span data-stu-id="2e0cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e0cd-122"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e0cd-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e0cd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e0cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e0cd-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2e0cd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0cd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e0cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0cd-126">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="2e0cd-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




