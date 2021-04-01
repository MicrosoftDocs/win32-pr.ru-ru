---
title: Сообщение WM_DDE_ACK (DDE. h)
description: 'Сообщение WM \_ DDE \_ ACK уведомляет о приложении платформа динамических данных Exchange (DDE) о получении и обработке следующих сообщений: приложение WM \_ DDE \_ , выполнение WM DDE, \_ \_ Данные WM \_ DDE, приложение \_ WM \_ DDE \_ advise, WM DDE unadvise \_ , \_ WM \_ DDE \_ INITIATE или \_ \_ запрос на DDE WM (в некоторых случаях). Чтобы опубликовать это сообщение, вызовите функцию почтовых сообщений со следующими параметрами.'
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Обмен данными с сообщениями WM_DDE_ACK
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071544"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="955c6-105">\_Сообщение WM DDE \_ ACK</span><span class="sxs-lookup"><span data-stu-id="955c6-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="955c6-106">Сообщение **WM \_ DDE \_ ACK** уведомляет приложение платформа динамических данных Exchange (DDE) о получении и обработке следующих сообщений: [**WM \_ DDE \_**](wm-dde-poke.md), [**\_ \_ выполнение WM DDE**](wm-dde-execute.md), [**\_ \_ Данные WM DDE**](wm-dde-data.md), приложение [**WM \_ DDE \_ advise**](wm-dde-advise.md), приложение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md), приложение [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)или [**\_ \_ запрос на DDE WM**](wm-dde-request.md) (в некоторых случаях).</span><span class="sxs-lookup"><span data-stu-id="955c6-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="955c6-107">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="955c6-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="955c6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="955c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="955c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="955c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="955c6-110">При ответе [**на \_ \_ Запуск команды WM DDE**](wm-dde-initiate.md)этот параметр является маркером серверного окна, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="955c6-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="955c6-111">При ответе [**на \_ \_ выполнение команды WM DDE**](wm-dde-execute.md)этот параметр является маркером для серверного окна, помещая сообщение.</span><span class="sxs-lookup"><span data-stu-id="955c6-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="955c6-112">При ответе на все остальные сообщения этот параметр является маркером клиентского или серверного окна, в котором размещается сообщение.</span><span class="sxs-lookup"><span data-stu-id="955c6-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="955c6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="955c6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="955c6-114">При ответе [**на \_ \_ Запуск программы WM DDE**](wm-dde-initiate.md), младшее слово содержит объект Atom, который идентифицирует ответное приложение.</span><span class="sxs-lookup"><span data-stu-id="955c6-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="955c6-115">Слово с высоким порядком содержит объект Atom, который определяет тему, для которой устанавливается диалог.</span><span class="sxs-lookup"><span data-stu-id="955c6-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="955c6-116">При ответе [**на \_ \_ выполнение приложения WM DDE**](wm-dde-execute.md)в нижнем порядке указывается структура [**ддеакк**](/windows/desktop/api/Dde/ns-dde-ddeack) , содержащая ряд флагов, которые указывают на состояние ответа.</span><span class="sxs-lookup"><span data-stu-id="955c6-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="955c6-117">Слово с высоким порядком является маркером глобального объекта памяти, который содержит командную строку, полученную в сообщении о **\_ \_ выполнении программы WM DDE** .</span><span class="sxs-lookup"><span data-stu-id="955c6-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="955c6-118">При ответе на все остальные сообщения слово низкого порядка указывает структуру [**ддеакк**](/windows/desktop/api/Dde/ns-dde-ddeack) , содержащую ряд флагов, которые указывают на состояние ответа.</span><span class="sxs-lookup"><span data-stu-id="955c6-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="955c6-119">Слово высокого порядка содержит глобальный объект Atom, который определяет имя элемента данных, для которого отправляется ответ.</span><span class="sxs-lookup"><span data-stu-id="955c6-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="955c6-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="955c6-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="955c6-121">Товаров</span><span class="sxs-lookup"><span data-stu-id="955c6-121">Posting</span></span>

<span data-ttu-id="955c6-122">За исключением ответа на [**сообщение \_ \_ запуска приложения WM DDE**](wm-dde-initiate.md) , приложение отправляет сообщение **WM \_ DDE \_ ACK** , вызывая функцию [**onmessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , а не вызывая функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="955c6-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="955c6-123">При ответе **на \_ \_ Запуск приложения WM DDE** приложение отправляет сообщение **WM \_ DDE \_ ACK** , вызывая **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="955c6-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="955c6-124">В этом случае ни имя приложения, ни Atom, ни имя раздела (Atom) не должны иметь **значение NULL** (даже если в сообщении, **\_ \_ запускающем DDE WM** , указано **значение NULL** атома).</span><span class="sxs-lookup"><span data-stu-id="955c6-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="955c6-125">При подтверждении любого сообщения с сопутствующим Atom приложение, размещая **WM \_ DDE \_ ACK** , может либо повторно использовать объект Atom, сопровождающий исходное сообщение, либо удалить его и создать новый.</span><span class="sxs-lookup"><span data-stu-id="955c6-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="955c6-126">При подтверждении [**\_ \_ выполнения приложения WM DDE**](wm-dde-execute.md)приложение, которое отправляет сообщение **WM \_ DDE \_ ACK** , должно повторно использовать объект глобальной памяти, определенный в исходном сообщении о **\_ \_ выполнении программы WM DDE** .</span><span class="sxs-lookup"><span data-stu-id="955c6-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="955c6-127">Все отправленные сообщения **WM \_ DDE с \_ подтверждением** должны создать или повторно использовать параметр *lParam* , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="955c6-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="955c6-128">Если приложение инициировало завершение диалога, отправляя сообщение [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) и ожидает подтверждения, ожидающее приложение не должно подтверждать (положительные или отрицательные) все последующие сообщения, отправленные другим приложением.</span><span class="sxs-lookup"><span data-stu-id="955c6-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="955c6-129">Ожидающее приложение должно удалить все атомы или объекты общей памяти, полученные в этих промежуточных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="955c6-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="955c6-130">Объекты памяти не должны освобождаться, если флаг **фрелеасе** имеет значение **false** в сообщениях [**\_ \_ данных DDE и WM**](wm-dde-data.md) DDE. [**\_ \_**](wm-dde-poke.md)</span><span class="sxs-lookup"><span data-stu-id="955c6-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="955c6-131">Получение</span><span class="sxs-lookup"><span data-stu-id="955c6-131">Receiving</span></span>

<span data-ttu-id="955c6-132">Приложение, получающее сообщение **WM \_ DDE \_ ACK** , должно удалить все атомы, сопровождающие сообщение.</span><span class="sxs-lookup"><span data-stu-id="955c6-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="955c6-133">Если приложение получает значение **WM \_ DDE \_ ACK** в ответ на сообщение с сопутствующим объектом глобальной памяти, а объект был отправлен с флагами **фрелеасе** , для которых задано **значение false**, приложение несет ответственность за удаление объекта.</span><span class="sxs-lookup"><span data-stu-id="955c6-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="955c6-134">Если приложение получает негативное сообщение **WM \_ DDE \_ ACK** , размещенное в ответ на сообщение с рекомендацией [**WM \_ DDE \_**](wm-dde-advise.md) , приложение должно удалить объект глобальной памяти, размещенный в исходном сообщении **WM \_ DDE \_ advise** .</span><span class="sxs-lookup"><span data-stu-id="955c6-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="955c6-135">Если приложение получает негативное сообщение **WM \_ DDE \_ ACK** , размещенное в ответ на [**\_ \_ данные DDE WM**](wm-dde-data.md), то приложение должно удалить объект глобальной памяти, размещенный в исходных **\_ \_ данных WM DDE**, **WM \_ DDE \_** или WM DDE, сообщение об **\_ \_ исполнении** . [**\_ \_**](wm-dde-poke.md) [**\_ \_**](wm-dde-execute.md)</span><span class="sxs-lookup"><span data-stu-id="955c6-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="955c6-136">Приложение, получающее отправленное сообщение **WM \_ DDE \_ ACK** , должно освободить параметр *lParam* с помощью функции [**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="955c6-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="955c6-137">Требования</span><span class="sxs-lookup"><span data-stu-id="955c6-137">Requirements</span></span>



| <span data-ttu-id="955c6-138">Требование</span><span class="sxs-lookup"><span data-stu-id="955c6-138">Requirement</span></span> | <span data-ttu-id="955c6-139">Значение</span><span class="sxs-lookup"><span data-stu-id="955c6-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="955c6-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="955c6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="955c6-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="955c6-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="955c6-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="955c6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="955c6-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="955c6-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="955c6-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="955c6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="955c6-145"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="955c6-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955c6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="955c6-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="955c6-147">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="955c6-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="955c6-148">**ддеакк**</span><span class="sxs-lookup"><span data-stu-id="955c6-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="955c6-149">**фридделпарам**</span><span class="sxs-lookup"><span data-stu-id="955c6-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="955c6-150">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="955c6-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="955c6-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="955c6-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="955c6-152">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="955c6-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="955c6-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="955c6-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="955c6-154">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="955c6-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="955c6-155">**Протокол WM \_ DDE \_ advise**</span><span class="sxs-lookup"><span data-stu-id="955c6-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="955c6-156">**\_данные DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="955c6-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="955c6-157">**\_выполнение WM DDE \_**</span><span class="sxs-lookup"><span data-stu-id="955c6-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="955c6-158">**\_Запуск WM DDE \_**</span><span class="sxs-lookup"><span data-stu-id="955c6-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="955c6-159">**\_Вставка DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="955c6-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="955c6-160">**\_запрос DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="955c6-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="955c6-161">**\_прерывание работы WM DDE \_**</span><span class="sxs-lookup"><span data-stu-id="955c6-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="955c6-162">**WM \_ DDE \_ unadvise**</span><span class="sxs-lookup"><span data-stu-id="955c6-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="955c6-163">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="955c6-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="955c6-164">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="955c6-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

