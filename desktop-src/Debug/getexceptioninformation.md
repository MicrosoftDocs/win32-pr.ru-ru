---
description: Извлекает независимое от компьютера описание исключения и сведения о состоянии компьютера, которое существует для потока при возникновении исключения. Эту функцию можно вызывать только в критерии фильтра обработчика исключений.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: Макрос Жетексцептионинформатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807817"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="b4e7e-104">Макрос Жетексцептионинформатион</span><span class="sxs-lookup"><span data-stu-id="b4e7e-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="b4e7e-105">Извлекает независимое от компьютера описание исключения и сведения о состоянии компьютера, которое существует для потока при возникновении исключения.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="b4e7e-106">Эту функцию можно вызывать только в критерии фильтра обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="b4e7e-107">Оптимизирующий компилятор Microsoft C/C++ интерпретирует эту функцию как ключевое слово, а ее использование вне соответствующего синтаксиса обработки исключений приводит к ошибке компилятора.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b4e7e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4e7e-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="b4e7e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4e7e-109">Parameters</span></span>

<span data-ttu-id="b4e7e-110">Этот макрос не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4e7e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4e7e-111">Return value</span></span>

<span data-ttu-id="b4e7e-112">Указатель на структуру [**\_ указателей исключений**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) , которая содержит указатели на следующие две структуры:</span><span class="sxs-lookup"><span data-stu-id="b4e7e-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="b4e7e-113">[**Исключение \_ Структура записи**](/windows/desktop/api/WinNT/ns-winnt-exception_record) , содержащая описание исключения.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="b4e7e-114">Структура [**контекста**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) , содержащая сведения о состоянии компьютера.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e7e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4e7e-115">Remarks</span></span>

<span data-ttu-id="b4e7e-116">Критерий фильтра (из которого вызывается функция) вычисляется при возникновении исключения во время выполнения блока **\_ \_ try** и определяет, выполняется ли блок **\_ \_ except** .</span><span class="sxs-lookup"><span data-stu-id="b4e7e-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="b4e7e-117">Критерий фильтра может вызывать функцию фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="b4e7e-118">Функция фильтра не может вызвать **жетексцептионинформатион**.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="b4e7e-119">Однако возвращаемое значение **жетексцептионинформатион** может быть передано в качестве параметра функции фильтра.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="b4e7e-120">Чтобы передать сведения [**об \_ указателях исключений**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) в блок обработчика исключений, выражение фильтра или функция Filter должны скопировать указатель или данные в надежное хранилище, к которому обработчику можно получить доступ позже.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="b4e7e-121">В случае вложенных обработчиков каждое критерий фильтра вычисляется до тех пор, пока одно выражение не будет оценено как **\_ \_ обработчик исключений** или **\_ продолжение \_ выполнения исключения**.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="b4e7e-122">Каждое выражение фильтра может вызывать **жетексцептионинформатион** для получения сведений об исключениях.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e7e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b4e7e-123">Requirements</span></span>



| <span data-ttu-id="b4e7e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b4e7e-124">Requirement</span></span> | <span data-ttu-id="b4e7e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e7e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4e7e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4e7e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e7e-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4e7e-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b4e7e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4e7e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e7e-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4e7e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4e7e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4e7e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e7e-131">**ЛОКАЛЬНОГО**</span><span class="sxs-lookup"><span data-stu-id="b4e7e-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="b4e7e-132">**\_указатели исключений**</span><span class="sxs-lookup"><span data-stu-id="b4e7e-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="b4e7e-133">**\_запись исключения**</span><span class="sxs-lookup"><span data-stu-id="b4e7e-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="b4e7e-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="b4e7e-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="b4e7e-135">**жетксстатефеатуресмаск**</span><span class="sxs-lookup"><span data-stu-id="b4e7e-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="b4e7e-136">Функции структурированной обработки исключений</span><span class="sxs-lookup"><span data-stu-id="b4e7e-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="b4e7e-137">Общие сведения об обработке структурированных исключений</span><span class="sxs-lookup"><span data-stu-id="b4e7e-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="b4e7e-138">Включить поддержку Windows для Intel AVX</span><span class="sxs-lookup"><span data-stu-id="b4e7e-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
