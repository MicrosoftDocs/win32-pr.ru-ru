---
description: Макрос НАПОМНИТЬ о создании напоминания во время компиляции. Этот макрос создает строку, содержащую строку параметра, имя исходного файла и номер строки.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: НАПОМНИТЬ (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688882"
---
# <a name="remind"></a><span data-ttu-id="4d230-104">Вам</span><span class="sxs-lookup"><span data-stu-id="4d230-104">REMIND</span></span>

<span data-ttu-id="4d230-105">`REMIND`Макрос создает напоминание во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="4d230-105">The `REMIND` macro generates a reminder at compile time.</span></span> <span data-ttu-id="4d230-106">Этот макрос создает строку, содержащую строку параметра, имя исходного файла и номер строки.</span><span class="sxs-lookup"><span data-stu-id="4d230-106">This macro generates a string that includes the parameter string, the name of the source file, and the line number.</span></span>

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="4d230-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d230-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d230-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*стрлитерал*</span><span class="sxs-lookup"><span data-stu-id="4d230-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="4d230-109">Текстовая строка.</span><span class="sxs-lookup"><span data-stu-id="4d230-109">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d230-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d230-110">Remarks</span></span>

<span data-ttu-id="4d230-111">Этот макрос полезен для создания предупреждений во время компиляции:</span><span class="sxs-lookup"><span data-stu-id="4d230-111">This macro is useful for generating compile-time warnings:</span></span>


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a><span data-ttu-id="4d230-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4d230-112">Requirements</span></span>



| <span data-ttu-id="4d230-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4d230-113">Requirement</span></span> | <span data-ttu-id="4d230-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4d230-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d230-115">Header</span><span class="sxs-lookup"><span data-stu-id="4d230-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4d230-116"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d230-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d230-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4d230-117">Library</span></span><br/> | <dl> <span data-ttu-id="4d230-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4d230-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d230-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d230-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d230-120">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="4d230-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




