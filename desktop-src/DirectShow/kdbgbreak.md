---
description: Вызывает исключение точки останова и записывает в журнал указанную строку с помощью макроса Дбглог. Игнорируется в розничных сборках.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Макрос Кдбгбреак (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685135"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="6957a-104">Макрос Кдбгбреак</span><span class="sxs-lookup"><span data-stu-id="6957a-104">KDbgBreak macro</span></span>

<span data-ttu-id="6957a-105">Вызывает исключение точки останова и записывает в журнал указанную строку с помощью макроса [**дбглог**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="6957a-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="6957a-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="6957a-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="6957a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6957a-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="6957a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6957a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6957a-109">*стрлитерал*</span><span class="sxs-lookup"><span data-stu-id="6957a-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="6957a-110">Текстовая строка.</span><span class="sxs-lookup"><span data-stu-id="6957a-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6957a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6957a-111">Return value</span></span>

<span data-ttu-id="6957a-112">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6957a-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6957a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6957a-113">Remarks</span></span>

<span data-ttu-id="6957a-114">В отличие от макроса [**дбгбреак**](dbgbreak.md) , этот макрос не отображает окно сообщения с запросом пользователя.</span><span class="sxs-lookup"><span data-stu-id="6957a-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="6957a-115">В отладочных сборках это автоматически приводит к возникновению исключения точки останова.</span><span class="sxs-lookup"><span data-stu-id="6957a-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="6957a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6957a-116">Requirements</span></span>



| <span data-ttu-id="6957a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6957a-117">Requirement</span></span> | <span data-ttu-id="6957a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6957a-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6957a-119">Header</span><span class="sxs-lookup"><span data-stu-id="6957a-119">Header</span></span><br/> | <dl> <span data-ttu-id="6957a-120"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6957a-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6957a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6957a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6957a-122">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="6957a-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




