---
title: Сообщение TB_SETPARENT (Коммктрл. h)
description: Задает окно, в котором элемент управления "панель инструментов" отправляет сообщения уведомления.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Элементы управления Windows для TB_SETPARENT сообщений
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892546"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="06153-104">\_Сообщение СЕТПАРЕНТ ТБ</span><span class="sxs-lookup"><span data-stu-id="06153-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="06153-105">Задает окно, в котором элемент управления "панель инструментов" отправляет сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="06153-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="06153-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06153-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06153-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06153-108">Обработчик окна для получения сообщений с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="06153-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="06153-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06153-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="06153-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="06153-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06153-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06153-111">Return value</span></span>

<span data-ttu-id="06153-112">Возвращаемое значение представляет собой обработчик предыдущего окна уведомления или **значение NULL** , если предыдущее окно уведомления отсутствует.</span><span class="sxs-lookup"><span data-stu-id="06153-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="06153-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06153-113">Remarks</span></span>

<span data-ttu-id="06153-114">Сообщение **\_ Сетпарент в ТБ** не изменяет родительское окно, указанное при создании элемента управления.</span><span class="sxs-lookup"><span data-stu-id="06153-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="06153-115">Вызов функции [**"**](/windows/desktop/api/winuser/nf-winuser-getparent) noreturn" для элемента управления ToolBar возвратит фактическое родительское окно, а не окно, указанное **в \_ сетпарент ТБ**.</span><span class="sxs-lookup"><span data-stu-id="06153-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="06153-116">Чтобы изменить родительское окно элемента управления, вызовите функцию [**сетпарент**](/windows/desktop/api/winuser/nf-winuser-setparent) .</span><span class="sxs-lookup"><span data-stu-id="06153-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06153-117">Требования</span><span class="sxs-lookup"><span data-stu-id="06153-117">Requirements</span></span>



| <span data-ttu-id="06153-118">Требование</span><span class="sxs-lookup"><span data-stu-id="06153-118">Requirement</span></span> | <span data-ttu-id="06153-119">Значение</span><span class="sxs-lookup"><span data-stu-id="06153-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06153-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06153-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06153-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06153-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06153-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06153-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06153-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06153-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06153-124">Header</span><span class="sxs-lookup"><span data-stu-id="06153-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="06153-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="06153-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

