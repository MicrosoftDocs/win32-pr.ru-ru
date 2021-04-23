---
title: Сообщение WM_DDE_UNADVISE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение WM \_ DDE \_ Unadvise для информирования серверного приложения DDE о том, что указанный элемент или определенный формат буфера обмена для элемента больше не должны обновляться.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Обмен данными с сообщениями WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492198"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="ccb3f-104">\_ \_ Сообщение об исходе DDE WM</span><span class="sxs-lookup"><span data-stu-id="ccb3f-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="ccb3f-105">Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **WM \_ DDE \_ unadvise** для информирования серверного приложения DDE о том, что указанный элемент или определенный формат буфера обмена для элемента больше не должны обновляться.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="ccb3f-106">В результате горячий или горячий канал данных для указанного элемента завершается.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="ccb3f-107">Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="ccb3f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccb3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb3f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccb3f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccb3f-110">Маркер клиентского окна, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="ccb3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccb3f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccb3f-112">Слово нижнего порядка указывает формат буфера обмена элемента, для которого отозван запрос на обновление.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="ccb3f-113">Если это **значение равно NULL**, все активные диалоги диалога [**WM \_ DDE \_**](wm-dde-advise.md) для элемента должны быть завершены.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="ccb3f-114">Слово высокого порядка содержит глобальный объект Atom, который определяет элемент, для которого отозван запрос на обновление.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="ccb3f-115">Если это **значение равно NULL**, все активные ссылки на предложение [**WM \_ DDE \_**](wm-dde-advise.md) , связанные с диалогом, должны быть завершены.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccb3f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccb3f-116">Remarks</span></span>

<span data-ttu-id="ccb3f-117">Клиентское приложение выделяет большое слово *lParam* с помощью вызова функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="ccb3f-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="ccb3f-118">Серверное приложение отправляет сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="ccb3f-119">При публикации **WM \_ DDE \_ ACK** сервер может либо повторно использовать Atom, либо удалить Atom и создать новый.</span><span class="sxs-lookup"><span data-stu-id="ccb3f-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb3f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ccb3f-120">Requirements</span></span>



| <span data-ttu-id="ccb3f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ccb3f-121">Requirement</span></span> | <span data-ttu-id="ccb3f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ccb3f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb3f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccb3f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb3f-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ccb3f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ccb3f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccb3f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb3f-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ccb3f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ccb3f-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ccb3f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccb3f-128"><dt>DDE. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccb3f-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb3f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccb3f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccb3f-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ccb3f-131">**глобаладдатом**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="ccb3f-132">**паккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="ccb3f-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="ccb3f-134">**реуседделпарам**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="ccb3f-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="ccb3f-136">**унпаккдделпарам**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="ccb3f-137">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="ccb3f-138">**Протокол WM \_ DDE \_ advise**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="ccb3f-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ccb3f-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ccb3f-140">Сведения о платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="ccb3f-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

