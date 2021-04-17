---
description: Логическое значение, указывающее, следует ли отслеживать эту блокировку.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Элемент Ккритсек:: m_fTrace (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657961"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="1bec2-103">Элемент Ккритсек:: m \_ фтраце</span><span class="sxs-lookup"><span data-stu-id="1bec2-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="1bec2-104">Логическое значение, указывающее, следует ли отслеживать эту блокировку.</span><span class="sxs-lookup"><span data-stu-id="1bec2-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bec2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bec2-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="1bec2-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bec2-106">Remarks</span></span>

<span data-ttu-id="1bec2-107">Эта переменная-член определена только в отладочной версии базового класса.</span><span class="sxs-lookup"><span data-stu-id="1bec2-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="1bec2-108">Если значение равно **true**, трассировка состояния блокировки записывается в журнал отладки.</span><span class="sxs-lookup"><span data-stu-id="1bec2-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="1bec2-109">(Журнал отладки для критически важных разделов должен быть активным.) Дополнительные сведения см. в разделе [**дбглокктраце**](dbglocktrace.md).</span><span class="sxs-lookup"><span data-stu-id="1bec2-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bec2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1bec2-110">Requirements</span></span>



| <span data-ttu-id="1bec2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1bec2-111">Requirement</span></span> | <span data-ttu-id="1bec2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1bec2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bec2-113">Header</span><span class="sxs-lookup"><span data-stu-id="1bec2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1bec2-114"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bec2-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1bec2-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1bec2-115">Library</span></span><br/> | <dl> <span data-ttu-id="1bec2-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1bec2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bec2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bec2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bec2-118">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="1bec2-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




