---
description: Вычисляет выражение в сборках Debug и Retail. В отладочных сборках отображает диагностическое сообщение, если выражение имеет значение FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Макрос EXECUTE_ASSERT (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652273"
---
# <a name="execute_assert-macro"></a><span data-ttu-id="3f427-104">ВЫПОЛНИТЬ \_ макрос assert</span><span class="sxs-lookup"><span data-stu-id="3f427-104">EXECUTE\_ASSERT macro</span></span>

<span data-ttu-id="3f427-105">Вычисляет выражение в сборках Debug и Retail.</span><span class="sxs-lookup"><span data-stu-id="3f427-105">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="3f427-106">В отладочных сборках отображает диагностическое сообщение, если выражение имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3f427-106">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f427-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f427-107">Syntax</span></span>


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="3f427-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f427-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f427-109">*cond*</span><span class="sxs-lookup"><span data-stu-id="3f427-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="3f427-110">Вычисляемое выражение.</span><span class="sxs-lookup"><span data-stu-id="3f427-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f427-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f427-111">Return value</span></span>

<span data-ttu-id="3f427-112">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3f427-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f427-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f427-113">Remarks</span></span>

<span data-ttu-id="3f427-114">В отличие от макроса [**Assert**](assert.md) , этот макрос вычисляет выражение в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="3f427-114">Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds.</span></span> <span data-ttu-id="3f427-115">Если в отладочных сборках выражение имеет **значение false**, макрос отображает окно сообщения с текстом выражения, именем исходного файла и номером строки.</span><span class="sxs-lookup"><span data-stu-id="3f427-115">In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="3f427-116">Пользователь может игнорировать утверждение, ввести отладчик или выйти из приложения.</span><span class="sxs-lookup"><span data-stu-id="3f427-116">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f427-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3f427-117">Requirements</span></span>



| <span data-ttu-id="3f427-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3f427-118">Requirement</span></span> | <span data-ttu-id="3f427-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3f427-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f427-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f427-120">Header</span></span><br/> | <dl> <span data-ttu-id="3f427-121"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f427-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f427-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f427-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f427-123">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="3f427-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




