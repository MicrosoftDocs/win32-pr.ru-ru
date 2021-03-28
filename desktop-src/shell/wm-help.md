---
description: Указывает, что пользователь нажал клавишу F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Сообщение WM_HELP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985392"
---
# <a name="wm_help-message"></a><span data-ttu-id="31b8c-103">\_Справочное сообщение WM</span><span class="sxs-lookup"><span data-stu-id="31b8c-103">WM\_HELP message</span></span>

<span data-ttu-id="31b8c-104">Указывает, что пользователь нажал клавишу F1.</span><span class="sxs-lookup"><span data-stu-id="31b8c-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="31b8c-105">Если при нажатии клавиши F1 меню активно, **\_ Справка WM** отправляется в окно, связанное с меню; в противном **случае \_ Справка WM** отправляется в окно, имеющее фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="31b8c-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="31b8c-106">Если ни один из окон не имеет фокуса клавиатуры, **\_ Справка WM** отправляется в текущее активное окно.</span><span class="sxs-lookup"><span data-stu-id="31b8c-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="31b8c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31b8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b8c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31b8c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31b8c-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="31b8c-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="31b8c-110">*лфи*</span><span class="sxs-lookup"><span data-stu-id="31b8c-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="31b8c-111">Адрес структуры [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) , содержащей сведения о пункте меню, элементе управления, диалоговом окне или окне, для которого запрашивается справка.</span><span class="sxs-lookup"><span data-stu-id="31b8c-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b8c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31b8c-112">Return value</span></span>

<span data-ttu-id="31b8c-113">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="31b8c-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31b8c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="31b8c-114">Remarks</span></span>

<span data-ttu-id="31b8c-115">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) передает **WM \_ справку** родительскому окну дочернего окна или владельцу окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="31b8c-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b8c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="31b8c-116">Requirements</span></span>



| <span data-ttu-id="31b8c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="31b8c-117">Requirement</span></span> | <span data-ttu-id="31b8c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="31b8c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31b8c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31b8c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31b8c-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31b8c-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="31b8c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31b8c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31b8c-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="31b8c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="31b8c-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="31b8c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b8c-124"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b8c-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 
