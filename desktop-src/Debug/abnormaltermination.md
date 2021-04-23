---
description: Указывает, \_ \_ завершается ли блок Try обработчика завершения в обычном режиме. Функцию можно вызывать только в \_ \_ блоке finally обработчика завершения.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: Макрос Абнормалтерминатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990721"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="8f785-104">Макрос Абнормалтерминатион</span><span class="sxs-lookup"><span data-stu-id="8f785-104">AbnormalTermination macro</span></span>

<span data-ttu-id="8f785-105">Указывает, завершается ли блок **\_ \_ try** обработчика завершения в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="8f785-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="8f785-106">Функцию можно вызывать только в блоке **\_ \_ finally** обработчика завершения.</span><span class="sxs-lookup"><span data-stu-id="8f785-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="8f785-107">Оптимизирующий компилятор Microsoft C/C++ интерпретирует эту функцию как ключевое слово, а ее использование вне соответствующего синтаксиса обработки исключений приводит к ошибке компилятора.</span><span class="sxs-lookup"><span data-stu-id="8f785-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8f785-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f785-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="8f785-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f785-109">Parameters</span></span>

<span data-ttu-id="8f785-110">Этот макрос не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8f785-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f785-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f785-111">Return value</span></span>

<span data-ttu-id="8f785-112">Если блок **\_ \_ try** аварийно завершает работу, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8f785-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="8f785-113">Если блок **\_ \_ try** завершается обычным образом, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8f785-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f785-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f785-114">Remarks</span></span>

<span data-ttu-id="8f785-115">Блок **\_ \_ try** обычно завершается, только если выполнение покидает блок последовательно после выполнения последней инструкции в блоке.</span><span class="sxs-lookup"><span data-stu-id="8f785-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="8f785-116">Инструкции (такие как **return**, **goto**, **Continue** или **break**), которые приводят к завершению блока **\_ \_ try** , вызывают аварийное завершение блока.</span><span class="sxs-lookup"><span data-stu-id="8f785-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="8f785-117">Это происходит, даже если такая инструкция является последней инструкцией в блоке **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="8f785-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="8f785-118">Аномальное завершение блока **\_ \_ try** приводит к тому, что система ищет в обратном направлении все кадры стека, чтобы определить, должны ли быть вызваны какие-либо обработчики завершения.</span><span class="sxs-lookup"><span data-stu-id="8f785-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="8f785-119">Это может привести к выполнению сотен инструкций, поэтому важно избегать аварийного завершения блока **\_ \_ try** из-за инструкций **return**, **goto**, **Continue** или **break** .</span><span class="sxs-lookup"><span data-stu-id="8f785-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="8f785-120">Обратите внимание, что эти инструкции не создают исключение, даже если завершение ненормально.</span><span class="sxs-lookup"><span data-stu-id="8f785-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="8f785-121">Чтобы избежать аварийного завершения, выполнение продолжается до конца блока.</span><span class="sxs-lookup"><span data-stu-id="8f785-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="8f785-122">Можно также выполнить инструкцию **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="8f785-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="8f785-123">Оператор **\_ \_ Leave** позволяет немедленно завершить блок **\_ \_ try** , не вызывая аварийного завершения и снижения его производительности.</span><span class="sxs-lookup"><span data-stu-id="8f785-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="8f785-124">Чтобы определить, поддерживается ли оператор **\_ \_ Leave** , проверьте документацию по компилятору.</span><span class="sxs-lookup"><span data-stu-id="8f785-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f785-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8f785-125">Requirements</span></span>



| <span data-ttu-id="8f785-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8f785-126">Requirement</span></span> | <span data-ttu-id="8f785-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8f785-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f785-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f785-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8f785-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8f785-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8f785-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f785-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8f785-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f785-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f785-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f785-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f785-133">Функции структурированной обработки исключений</span><span class="sxs-lookup"><span data-stu-id="8f785-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="8f785-134">Общие сведения об обработке структурированных исключений</span><span class="sxs-lookup"><span data-stu-id="8f785-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




