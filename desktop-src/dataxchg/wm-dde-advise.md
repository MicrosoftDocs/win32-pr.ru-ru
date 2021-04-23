---
title: Сообщение WM_DDE_ADVISE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение об ошибке WM DDE в приложение сервера DDE, чтобы запрашивать сервер предоставлять обновление для элемента данных при каждом изменении элемента.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Обмен данными с сообщениями WM_DDE_ADVISE
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135751"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="73410-104">\_ \_ Сообщение об исходе DDE WM</span><span class="sxs-lookup"><span data-stu-id="73410-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="73410-105">Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение об ошибке **WM \_ DDE \_** в приложение сервера DDE, чтобы запрашивать сервер предоставлять обновление для элемента данных при каждом изменении элемента.</span><span class="sxs-lookup"><span data-stu-id="73410-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="73410-106">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="73410-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="73410-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="73410-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73410-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73410-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73410-109">Обработчик, помещая сообщение в клиентское окно.</span><span class="sxs-lookup"><span data-stu-id="73410-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="73410-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73410-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73410-111">Слово низкого порядка является маркером глобального объекта памяти, содержащего структуру [**ддеадвисе**](/windows/desktop/api/Dde/ns-dde-ddeadvise) , указывающую способ отправки данных.</span><span class="sxs-lookup"><span data-stu-id="73410-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="73410-112">Слово высокого порядка содержит объект Atom, который идентифицирует запрошенный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="73410-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73410-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73410-113">Remarks</span></span>

<span data-ttu-id="73410-114">Если клиентское приложение поддерживает несколько форматов буфера обмена для одного раздела и элемента, оно может отправлять несколько сообщений с рекомендацией **WM \_ DDE \_** для раздела и элемента, указывая другой формат буфера обмена для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="73410-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="73410-115">Обратите внимание, что сервер может поддерживать несколько форматов только для ссылок на горячие данные, а не для горячих ссылок на данные.</span><span class="sxs-lookup"><span data-stu-id="73410-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="73410-116">Товаров</span><span class="sxs-lookup"><span data-stu-id="73410-116">Posting</span></span>

<span data-ttu-id="73410-117">Клиентское приложение отправляет сообщение с рекомендацией **WM \_ DDE \_** с помощью вызова функции [**onmessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , а не функции [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="73410-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="73410-118">Клиентское приложение выделяет объект глобальной памяти с помощью функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="73410-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="73410-119">Он выделяет Atom с помощью функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="73410-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="73410-120">Клиентское приложение должно создать или повторно использовать **параметр \_ WM DDE \_ advise** *lParam* , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="73410-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="73410-121">Если принимающее (серверное) приложение получает ответ с отрицательным сообщением [**WM \_ DDE \_**](wm-dde-ack.md) , оно должно удалить объект.</span><span class="sxs-lookup"><span data-stu-id="73410-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="73410-122">Флаг **фрелеасе** не используется в сообщениях с рекомендацией **WM \_ DDE \_** , но их поведение при освобождении данных аналогично поведению [**\_ \_ данных WM DDE**](wm-dde-data.md) , и сообщения [**WM \_ DDE \_**](wm-dde-poke.md) , где **фрелеасе** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="73410-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="73410-123">Получение</span><span class="sxs-lookup"><span data-stu-id="73410-123">Receiving</span></span>

<span data-ttu-id="73410-124">Серверное приложение отправляет сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа.</span><span class="sxs-lookup"><span data-stu-id="73410-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="73410-125">При отправке приложения **WM \_ DDE \_ ACK** приложение может повторно использовать Atom или удалить его и создать новый.</span><span class="sxs-lookup"><span data-stu-id="73410-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="73410-126">Если сообщение **WM \_ DDE \_** имеет положительное значение, приложение должно удалить объект глобальной памяти; в противном случае приложение не должно удалять объект.</span><span class="sxs-lookup"><span data-stu-id="73410-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="73410-127">Сервер должен создать или повторно использовать параметр *lParam* в [**WM \_ DDE \_**](wm-dde-ack.md) , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="73410-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="73410-128">Требования</span><span class="sxs-lookup"><span data-stu-id="73410-128">Requirements</span></span>



| <span data-ttu-id="73410-129">Требование</span><span class="sxs-lookup"><span data-stu-id="73410-129">Requirement</span></span> | <span data-ttu-id="73410-130">Значение</span><span class="sxs-lookup"><span data-stu-id="73410-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73410-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73410-131">Minimum supported client</span></span><br/> | <span data-ttu-id="73410-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="73410-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="73410-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73410-133">Minimum supported server</span></span><br/> | <span data-ttu-id="73410-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="73410-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="73410-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="73410-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="73410-136"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73410-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73410-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73410-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="73410-138">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="73410-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73410-139">**ддеадвисе**</span><span class="sxs-lookup"><span data-stu-id="73410-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="73410-140">**фридделпарам**</span><span class="sxs-lookup"><span data-stu-id="73410-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="73410-141">**глобаладдатом**</span><span class="sxs-lookup"><span data-stu-id="73410-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="73410-142">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="73410-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="73410-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="73410-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="73410-144">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="73410-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="73410-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="73410-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="73410-146">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="73410-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="73410-147">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="73410-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="73410-148">**\_данные DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="73410-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="73410-149">**\_Вставка DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="73410-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="73410-150">**\_запрос DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="73410-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="73410-151">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="73410-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73410-152">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="73410-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

