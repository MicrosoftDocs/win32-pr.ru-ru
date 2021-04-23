---
title: Сообщение WM_DDE_DATA (DDE. h)
description: Серверное приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение данных WM DDE в клиентское приложение DDE для передачи элемента данных клиенту или для уведомления клиента о доступности элемента данных.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- Обмен данными с сообщениями WM_DDE_DATA
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710486"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="e9aec-104">\_ \_ Сообщение данных DDE WM</span><span class="sxs-lookup"><span data-stu-id="e9aec-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="e9aec-105">Серверное приложение платформа динамических данных Exchange (DDE) отправляет сообщение **\_ \_ данных WM DDE** в клиентское приложение DDE для передачи элемента данных клиенту или для уведомления клиента о доступности элемента данных.</span><span class="sxs-lookup"><span data-stu-id="e9aec-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="e9aec-106">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="e9aec-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="e9aec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9aec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9aec-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9aec-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9aec-109">Маркер серверного окна, помещая сообщение.</span><span class="sxs-lookup"><span data-stu-id="e9aec-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="e9aec-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9aec-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9aec-111">Слово низкого порядка — это маркер глобального объекта памяти, содержащего структуру [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) с данными и дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e9aec-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="e9aec-112">Если сервер уведомляет клиента о том, что значение элемента данных изменилось во время канала горячего передачи данных, этот обработчик должен иметь значение **null** .</span><span class="sxs-lookup"><span data-stu-id="e9aec-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="e9aec-113">Горячий канал устанавливается клиентом, отправляющей сообщение [**WM \_ DDE \_ advise**](wm-dde-advise.md) с установленным битом **фдеферупд** .</span><span class="sxs-lookup"><span data-stu-id="e9aec-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="e9aec-114">Слово высокого порядка содержит объект Atom, который определяет элемент данных, для которого отправляются данные или уведомление.</span><span class="sxs-lookup"><span data-stu-id="e9aec-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9aec-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9aec-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="e9aec-116">Товаров</span><span class="sxs-lookup"><span data-stu-id="e9aec-116">Posting</span></span>

<span data-ttu-id="e9aec-117">Серверное приложение выделяет объект глобальной памяти с помощью функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="e9aec-118">Он выделяет Atom с помощью функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="e9aec-119">Сервер должен создать или повторно использовать параметр *lParam* для **\_ \_ данных WM DDE** , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="e9aec-120">Если принимающее (клиентское) приложение реагирует на отрицательное [**сообщение \_ WM \_ DDE**](wm-dde-ack.md) , приложение, выполняющее разноски (сервер), должно удалить объект глобальной памяти. в противном случае клиент должен удалить объект после извлечения его содержимого, вызвав функцию [**унпаккдделпарам**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="e9aec-121">Если серверное приложение устанавливает для элемента **фрелеасе** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) **значение false**, сервер несет ответственность за удаление объекта при получении положительного или отрицательного подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e9aec-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="e9aec-122">Серверному приложению не следует задавать значения **false** для членов **факкрек** и **фрелеасе** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="e9aec-123">Если для обоих членов задано **значение false**, сервер не может определить, когда следует удалить объект.</span><span class="sxs-lookup"><span data-stu-id="e9aec-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="e9aec-124">Получение</span><span class="sxs-lookup"><span data-stu-id="e9aec-124">Receiving</span></span>

<span data-ttu-id="e9aec-125">Если **факкрек** имеет **значение true**, клиентское приложение должно отправлять ответное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа.</span><span class="sxs-lookup"><span data-stu-id="e9aec-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="e9aec-126">При размещении **WM \_ DDE \_ ACK** клиент может либо повторно использовать Atom, либо удалить его и создать новый.</span><span class="sxs-lookup"><span data-stu-id="e9aec-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="e9aec-127">Клиент должен создать или повторно использовать параметр *lParam* в [**WM \_ DDE \_**](wm-dde-ack.md) , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="e9aec-128">Если **факкрек** имеет **значение false**, клиентское приложение должно удалить Atom.</span><span class="sxs-lookup"><span data-stu-id="e9aec-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="e9aec-129">Если в приложении, указанном в параметре Global Memory, задано **значение NULL**, принимающее приложение может запросить у сервера отправить данные путем отправки сообщения [**\_ \_ запроса DDE WM**](wm-dde-request.md) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="e9aec-130">После обработки сообщения **\_ \_ данных WM DDE** , в котором объект глобальной памяти не имеет **значение NULL**, клиент должен освободить объект, если не выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="e9aec-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="e9aec-131">Член **фрелеасе** имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e9aec-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="e9aec-132">Член **фрелеасе** имеет **значение true**, но клиентское приложение реагирует на сообщение о неотрицательном сообщении [**WM \_ DDE \_**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="e9aec-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9aec-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e9aec-133">Requirements</span></span>



| <span data-ttu-id="e9aec-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e9aec-134">Requirement</span></span> | <span data-ttu-id="e9aec-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e9aec-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9aec-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9aec-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e9aec-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9aec-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e9aec-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9aec-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e9aec-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9aec-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9aec-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e9aec-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9aec-141"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9aec-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9aec-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9aec-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9aec-143">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e9aec-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9aec-144">**ддедата**</span><span class="sxs-lookup"><span data-stu-id="e9aec-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="e9aec-145">**фридделпарам**</span><span class="sxs-lookup"><span data-stu-id="e9aec-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="e9aec-146">**глобаладдатом**</span><span class="sxs-lookup"><span data-stu-id="e9aec-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="e9aec-147">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="e9aec-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="e9aec-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="e9aec-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="e9aec-149">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="e9aec-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="e9aec-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="e9aec-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="e9aec-151">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="e9aec-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="e9aec-152">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="e9aec-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="e9aec-153">**Протокол WM \_ DDE \_ advise**</span><span class="sxs-lookup"><span data-stu-id="e9aec-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="e9aec-154">**\_Вставка DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e9aec-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="e9aec-155">**\_запрос DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e9aec-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="e9aec-156">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e9aec-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9aec-157">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="e9aec-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

