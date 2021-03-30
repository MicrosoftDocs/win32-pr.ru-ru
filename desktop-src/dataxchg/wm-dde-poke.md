---
title: Сообщение WM_DDE_POKE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение WM \_ DDE \_ в приложение сервера DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Обмен данными с сообщениями WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803922"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="a3463-104">\_Сообщение о \_ выводится DDE WM</span><span class="sxs-lookup"><span data-stu-id="a3463-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="a3463-105">Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **WM \_ DDE \_** в приложение сервера DDE.</span><span class="sxs-lookup"><span data-stu-id="a3463-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="a3463-106">Клиент использует это сообщение, чтобы запросить сервер на прием незапрошенного элемента данных.</span><span class="sxs-lookup"><span data-stu-id="a3463-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="a3463-107">Ожидается, что сервер отвечает с сообщением [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , указывающим, принял ли он элемент данных.</span><span class="sxs-lookup"><span data-stu-id="a3463-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="a3463-108">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="a3463-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="a3463-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3463-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3463-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3463-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3463-111">Обработчик, помещая сообщение в клиентское окно.</span><span class="sxs-lookup"><span data-stu-id="a3463-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="a3463-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3463-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3463-113">Слово низкого порядка — это маркер глобального объекта памяти, содержащего структуру [**ддепоке**](/windows/desktop/api/Dde/ns-dde-ddepoke) с данными и дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a3463-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="a3463-114">Слово высокого порядка содержит глобальный объект Atom, который определяет элемент данных, для которого отправляются данные или уведомление.</span><span class="sxs-lookup"><span data-stu-id="a3463-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3463-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3463-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="a3463-116">Товаров</span><span class="sxs-lookup"><span data-stu-id="a3463-116">Posting</span></span>

<span data-ttu-id="a3463-117">Клиентское приложение должно выделить память для объекта глобальной памяти с помощью функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="a3463-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="a3463-118">Клиентское приложение должно удалить объект, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="a3463-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="a3463-119">Серверное приложение реагирует на отрицательное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="a3463-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="a3463-120">Член **фрелеасе** имеет **значение false**, но серверное приложение реагирует на положительный или отрицательный ответ [**WM \_ DDE \_**](wm-dde-ack.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="a3463-121">Клиентское приложение должно создать Atom с помощью функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="a3463-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="a3463-122">Клиентское приложение должно создать или повторно использовать **параметр \_ WM \_ DDE** с параметрами *lParam* , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="a3463-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="a3463-123">Получение</span><span class="sxs-lookup"><span data-stu-id="a3463-123">Receiving</span></span>

<span data-ttu-id="a3463-124">Серверное приложение должно отправлять ответное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа.</span><span class="sxs-lookup"><span data-stu-id="a3463-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="a3463-125">При размещении **WM \_ DDE \_ ACK** сервер может либо повторно использовать Atom, либо удалить его и создать новый.</span><span class="sxs-lookup"><span data-stu-id="a3463-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="a3463-126">Сервер должен создать или повторно использовать параметр *lParam* в [**WM \_ DDE \_**](wm-dde-ack.md) , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="a3463-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="a3463-127">Чтобы освободить объект глобальной памяти, сервер должен вызвать функцию [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="a3463-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="a3463-128">Кроме того, если формат данных — [**CF \_ Дспметафилепикт**](clipboard-formats.md) или **CF \_ метафилепикт**, сервер также должен вызвать [**делетеметафиле**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) с помощью внедренного метафайла.</span><span class="sxs-lookup"><span data-stu-id="a3463-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="a3463-129">Эти два формата имеют дополнительный уровень косвенного обращения. то есть приложение должно заблокировать объект для получения указателя на маркер, а затем заблокировать этот обработчик для получения указателя на структуру [**метафилепикт**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) и, наконец, вызвать **делетеметафиле** с помощью маркера из **ХМФ** элемента структуры **метафилепикт** .</span><span class="sxs-lookup"><span data-stu-id="a3463-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="a3463-130">Чтобы освободить объект, сервер должен вызвать функцию [**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="a3463-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3463-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a3463-131">Requirements</span></span>



| <span data-ttu-id="a3463-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a3463-132">Requirement</span></span> | <span data-ttu-id="a3463-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a3463-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3463-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3463-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a3463-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3463-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a3463-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3463-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a3463-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3463-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3463-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3463-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3463-139"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3463-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3463-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3463-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3463-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a3463-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3463-142">**ддепоке**</span><span class="sxs-lookup"><span data-stu-id="a3463-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="a3463-143">**фридделпарам**</span><span class="sxs-lookup"><span data-stu-id="a3463-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="a3463-144">**глобаладдатом**</span><span class="sxs-lookup"><span data-stu-id="a3463-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="a3463-145">**метафилепикт**</span><span class="sxs-lookup"><span data-stu-id="a3463-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="a3463-146">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="a3463-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="a3463-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="a3463-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="a3463-148">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="a3463-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="a3463-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="a3463-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="a3463-150">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="a3463-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="a3463-151">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="a3463-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="a3463-152">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a3463-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3463-153">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="a3463-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

