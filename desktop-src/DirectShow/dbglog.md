---
description: Макрос Дбглог отправляет строку в расположение выходных данных отладки, если ведение журнала включено для указанного типа и уровня. Этот макрос не учитывается в розничных сборках.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Макрос Дбглог (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675402"
---
# <a name="dbglog-macro"></a><span data-ttu-id="9a1c8-104">Макрос Дбглог</span><span class="sxs-lookup"><span data-stu-id="9a1c8-104">DbgLog macro</span></span>

<span data-ttu-id="9a1c8-105">Макрос **дбглог** отправляет строку в расположение выходных данных отладки, если ведение журнала включено для указанного типа и уровня.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="9a1c8-106">Этот макрос не учитывается в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a1c8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a1c8-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="9a1c8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a1c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a1c8-109">*Типы*</span><span class="sxs-lookup"><span data-stu-id="9a1c8-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1c8-110">Побитовое сочетание одного или нескольких типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="9a1c8-111">*Уровень*</span><span class="sxs-lookup"><span data-stu-id="9a1c8-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1c8-112">Уровень ведения журнала для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="9a1c8-113">*пформат*</span><span class="sxs-lookup"><span data-stu-id="9a1c8-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1c8-114">Строка формата в стиле **printf** .</span><span class="sxs-lookup"><span data-stu-id="9a1c8-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="9a1c8-115">*...*</span><span class="sxs-lookup"><span data-stu-id="9a1c8-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1c8-116">Дополнительные аргументы для строки формата.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a1c8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a1c8-117">Return value</span></span>

<span data-ttu-id="9a1c8-118">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a1c8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a1c8-119">Remarks</span></span>

<span data-ttu-id="9a1c8-120">Если для журнала отладки любого из типов сообщений задан указанный уровень или выше, этот макрос отправляет отформатированную строку в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="9a1c8-121">Макрос автоматически добавляет символ новой строки в выходную строку.</span><span class="sxs-lookup"><span data-stu-id="9a1c8-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="9a1c8-122">Параметры макроса должны заключаться в дополнительный набор круглых скобок:</span><span class="sxs-lookup"><span data-stu-id="9a1c8-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="9a1c8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9a1c8-123">Requirements</span></span>



| <span data-ttu-id="9a1c8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9a1c8-124">Requirement</span></span> | <span data-ttu-id="9a1c8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9a1c8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a1c8-126">Header</span><span class="sxs-lookup"><span data-stu-id="9a1c8-126">Header</span></span><br/> | <dl> <span data-ttu-id="9a1c8-127"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a1c8-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a1c8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a1c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1c8-129">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="9a1c8-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




