---
title: Сообщение WM_DDE_TERMINATE (DDE. h)
description: Приложение платформа динамических данных Exchange (клиент или сервер) отправляет \_ \_ сообщение об увольнении WM DDE для завершения диалога. Чтобы опубликовать это сообщение, вызовите функцию почтовых сообщений со следующими параметрами.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Обмен данными с сообщениями WM_DDE_TERMINATE
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135647"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="c7911-105">\_Сообщение о \_ прекращении DDE в WM</span><span class="sxs-lookup"><span data-stu-id="c7911-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="c7911-106">Приложение платформа динамических данных Exchange (клиент или сервер) отправляет сообщение об **\_ \_ увольнении WM DDE** для завершения диалога.</span><span class="sxs-lookup"><span data-stu-id="c7911-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="c7911-107">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c7911-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="c7911-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7911-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7911-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7911-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7911-110">Маркер для клиентского или серверного окна, в котором разноски сообщения.</span><span class="sxs-lookup"><span data-stu-id="c7911-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="c7911-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7911-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7911-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c7911-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7911-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7911-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="c7911-114">Товаров</span><span class="sxs-lookup"><span data-stu-id="c7911-114">Posting</span></span>

<span data-ttu-id="c7911-115">При ожидании подтверждения завершения приложение не должно отправлять другие сообщения в принимающее приложение.</span><span class="sxs-lookup"><span data-stu-id="c7911-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="c7911-116">Если отправляющее приложение получает сообщения (отличные от **WM \_ DDE \_**) от принимающего приложения, то оно должно удалить все атомы или объекты общей памяти, сопровождающие сообщения, за исключением глобальных объектов памяти, связанных с сообщениями об ошибках в приложениях [**WM \_ DDE \_**](wm-dde-poke.md) или [**WM \_ \_**](wm-dde-data.md) DDE, не имеющих набора элементов **фрелеасе** .</span><span class="sxs-lookup"><span data-stu-id="c7911-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="c7911-117">Получение</span><span class="sxs-lookup"><span data-stu-id="c7911-117">Receiving</span></span>

<span data-ttu-id="c7911-118">Клиентское или серверное приложение должно отвечать, отправляя сообщение о **\_ \_ прекращении работы WM DDE** .</span><span class="sxs-lookup"><span data-stu-id="c7911-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7911-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c7911-119">Requirements</span></span>



| <span data-ttu-id="c7911-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c7911-120">Requirement</span></span> | <span data-ttu-id="c7911-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c7911-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7911-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7911-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7911-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7911-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c7911-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7911-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7911-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7911-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7911-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c7911-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7911-127"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7911-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7911-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7911-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7911-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c7911-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7911-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="c7911-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="c7911-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c7911-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="c7911-132">**\_данные DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="c7911-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="c7911-133">**\_Вставка DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="c7911-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="c7911-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c7911-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7911-135">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="c7911-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

