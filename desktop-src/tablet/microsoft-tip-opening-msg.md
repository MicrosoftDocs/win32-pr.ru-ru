---
description: Уведомляет окно при открытии панели ввода текста.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Сообщение MICROSOFT_TIP_OPENING_MSG (Пенинпутпанел. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718141"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="216f6-103">\_Сообщение о \_ открывающем сообщении Microsoft TIP \_</span><span class="sxs-lookup"><span data-stu-id="216f6-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="216f6-104">Уведомляет окно при открытии панели ввода текста.</span><span class="sxs-lookup"><span data-stu-id="216f6-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="216f6-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="216f6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216f6-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="216f6-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="216f6-107">В настоящее время не используется, должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="216f6-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="216f6-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="216f6-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="216f6-109">В настоящее время не используется, должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="216f6-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216f6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="216f6-110">Return value</span></span>

<span data-ttu-id="216f6-111">Приложения должны вызвать [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) после обработки этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="216f6-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="216f6-112">Сведения о возвращаемых значениях см. в разделе **дефвиндовпрок** .</span><span class="sxs-lookup"><span data-stu-id="216f6-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="216f6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="216f6-113">Remarks</span></span>

<span data-ttu-id="216f6-114">Это уведомление позволяет получить сведения о том, когда открывается панель ввода.</span><span class="sxs-lookup"><span data-stu-id="216f6-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="216f6-115">Если вы хотите выполнить действие в этом случае, обработайте сообщение, выполните операцию в обработчике, а затем передайте сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="216f6-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="216f6-116">Это сообщение также отправляется, когда панель ввода текста уже отображается и пользователь переключается с клавиатуры на обложку рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="216f6-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="216f6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="216f6-117">Requirements</span></span>



| <span data-ttu-id="216f6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="216f6-118">Requirement</span></span> | <span data-ttu-id="216f6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="216f6-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="216f6-120">Клиент</span><span class="sxs-lookup"><span data-stu-id="216f6-120">Client</span></span><br/> | <span data-ttu-id="216f6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="216f6-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="216f6-122">Header</span><span class="sxs-lookup"><span data-stu-id="216f6-122">Header</span></span><br/> | <dl> <span data-ttu-id="216f6-123"><dt>Пенинпутпанел. h</dt></span><span class="sxs-lookup"><span data-stu-id="216f6-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 

