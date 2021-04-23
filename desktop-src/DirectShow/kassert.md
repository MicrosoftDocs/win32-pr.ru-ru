---
description: Вычисляет выражение и вызывает исключение точки останова, если выражение имеет значение FALSE. Текст выражения, имя исходного файла и номер строки записываются с помощью макроса Дбглог. Игнорируется в розничных сборках.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Макрос КАССЕРТ (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680001"
---
# <a name="kassert-macro"></a><span data-ttu-id="249eb-105">Макрос КАССЕРТ</span><span class="sxs-lookup"><span data-stu-id="249eb-105">KASSERT macro</span></span>

<span data-ttu-id="249eb-106">Вычисляет выражение и вызывает исключение точки останова, если выражение имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="249eb-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="249eb-107">Текст выражения, имя исходного файла и номер строки записываются с помощью макроса [**дбглог**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="249eb-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="249eb-108">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="249eb-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="249eb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="249eb-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="249eb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="249eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="249eb-111">*cond*</span><span class="sxs-lookup"><span data-stu-id="249eb-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="249eb-112">Вычисляемое выражение.</span><span class="sxs-lookup"><span data-stu-id="249eb-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="249eb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="249eb-113">Return value</span></span>

<span data-ttu-id="249eb-114">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="249eb-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="249eb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="249eb-115">Remarks</span></span>

<span data-ttu-id="249eb-116">В отличие от макроса [**Assert**](assert.md) и [**Execute \_ Assert**](execute-assert.md) , этот макрос не отображает окно сообщения с запросом пользователя.</span><span class="sxs-lookup"><span data-stu-id="249eb-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="249eb-117">В отладочных сборках, если выражение имеет **значение false**, макрос автоматически вызывает исключение точки останова.</span><span class="sxs-lookup"><span data-stu-id="249eb-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="249eb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="249eb-118">Requirements</span></span>



| <span data-ttu-id="249eb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="249eb-119">Requirement</span></span> | <span data-ttu-id="249eb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="249eb-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="249eb-121">Header</span><span class="sxs-lookup"><span data-stu-id="249eb-121">Header</span></span><br/> | <dl> <span data-ttu-id="249eb-122"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="249eb-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249eb-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="249eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249eb-124">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="249eb-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




