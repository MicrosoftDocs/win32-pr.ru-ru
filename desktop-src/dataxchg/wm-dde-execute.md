---
title: Сообщение WM_DDE_EXECUTE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение выполнения WM DDE в приложение сервера DDE, чтобы отправить строку на сервер для обработки в виде последовательности команд.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Обмен данными с сообщениями WM_DDE_EXECUTE
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415660"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="d0014-104">\_Сообщение о выполнении DDE в WM \_</span><span class="sxs-lookup"><span data-stu-id="d0014-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="d0014-105">Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **\_ \_ выполнения WM DDE** в приложение сервера DDE, чтобы отправить строку на сервер для обработки в виде последовательности команд.</span><span class="sxs-lookup"><span data-stu-id="d0014-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="d0014-106">Серверное приложение должно публиковать в ответе сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="d0014-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="d0014-107">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="d0014-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="d0014-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0014-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0014-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0014-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0014-110">Обработчик, помещая сообщение в клиентское окно.</span><span class="sxs-lookup"><span data-stu-id="d0014-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="d0014-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0014-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0014-112">Содержит объект глобальной памяти, который ссылается на командную строку ANSI или Unicode в зависимости от типов окон, участвующих в диалоге.</span><span class="sxs-lookup"><span data-stu-id="d0014-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0014-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0014-113">Remarks</span></span>

<span data-ttu-id="d0014-114">Командная строка — это строка, завершающаяся нулем, состоящая из одной или нескольких строк кода операций, заключенных в одинарные скобки ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="d0014-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="d0014-115">Каждая строка кода операции имеет следующий синтаксис, где список *параметров* является необязательным:</span><span class="sxs-lookup"><span data-stu-id="d0014-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="d0014-116">*параметры кода операции*</span><span class="sxs-lookup"><span data-stu-id="d0014-116">*opcode parameters*</span></span>

<span data-ttu-id="d0014-117">*Код операции* — это любой определенный приложением один токен.</span><span class="sxs-lookup"><span data-stu-id="d0014-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="d0014-118">Он не может содержать пробелы, запятые, круглые скобки, квадратные скобки или кавычки.</span><span class="sxs-lookup"><span data-stu-id="d0014-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="d0014-119">Список *Parameters* может содержать любые значения, определенные приложением.</span><span class="sxs-lookup"><span data-stu-id="d0014-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="d0014-120">Несколько параметров разделяются запятыми, а весь список параметров заключается в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="d0014-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="d0014-121">Параметры не могут содержать запятые или круглые скобки, за исключением строк в кавычках.</span><span class="sxs-lookup"><span data-stu-id="d0014-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="d0014-122">Если квадратная скобка или скобка должна появляться в строке в кавычках, она не должна быть двойной, как в случае с старыми правилами.</span><span class="sxs-lookup"><span data-stu-id="d0014-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="d0014-123">Ниже приведены допустимые командные строки.</span><span class="sxs-lookup"><span data-stu-id="d0014-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="d0014-124">Обратите внимание, что в старых правилах круглые скобки и скобки должны быть двойными, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d0014-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="d0014-125">Серверы должны иметь возможность анализировать команды в любой форме.</span><span class="sxs-lookup"><span data-stu-id="d0014-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="d0014-126">Строки выполнения в Юникоде следует использовать, только если дескрипторы окна клиента и сервера приводят к тому, что функция [**исвиндовуникоде**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d0014-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="d0014-127">Товаров</span><span class="sxs-lookup"><span data-stu-id="d0014-127">Posting</span></span>

<span data-ttu-id="d0014-128">Клиентское приложение выделяет объект глобальной памяти путем вызова функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="d0014-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="d0014-129">При обработке сообщения [**WM \_ DDE \_ ACK**](wm-dde-ack.md) о том, что сервер отправляет ответ на сообщение **\_ \_ выполнения WM DDE** , клиентское приложение должно удалить объект, возвращенный сообщением **WM \_ DDE \_ ACK** .</span><span class="sxs-lookup"><span data-stu-id="d0014-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="d0014-130">Получение</span><span class="sxs-lookup"><span data-stu-id="d0014-130">Receiving</span></span>

<span data-ttu-id="d0014-131">Серверное приложение отправляет сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа.</span><span class="sxs-lookup"><span data-stu-id="d0014-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="d0014-132">Сервер должен повторно использовать объект глобальной памяти.</span><span class="sxs-lookup"><span data-stu-id="d0014-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="d0014-133">Если не указано иное по подпротоколу, сервер не должен публиковать сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) до тех пор, пока не будут завершены все действия, указанные в командной строке выполнения.</span><span class="sxs-lookup"><span data-stu-id="d0014-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="d0014-134">Единственным исключением из этого правила является то, что строка заставляет сервер завершить диалог.</span><span class="sxs-lookup"><span data-stu-id="d0014-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0014-135">Требования</span><span class="sxs-lookup"><span data-stu-id="d0014-135">Requirements</span></span>



| <span data-ttu-id="d0014-136">Требование</span><span class="sxs-lookup"><span data-stu-id="d0014-136">Requirement</span></span> | <span data-ttu-id="d0014-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d0014-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0014-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0014-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0014-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0014-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d0014-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0014-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0014-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0014-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d0014-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d0014-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0014-143"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0014-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0014-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0014-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0014-145">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d0014-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d0014-146">**исвиндовуникоде**</span><span class="sxs-lookup"><span data-stu-id="d0014-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="d0014-147">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="d0014-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="d0014-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="d0014-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="d0014-149">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="d0014-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="d0014-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="d0014-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="d0014-151">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="d0014-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="d0014-152">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="d0014-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="d0014-153">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d0014-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d0014-154">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="d0014-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

