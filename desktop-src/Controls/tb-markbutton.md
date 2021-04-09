---
title: Сообщение TB_MARKBUTTON (Коммктрл. h)
description: Задает состояние выделения для данной кнопки в элементе управления ToolBar.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- Элементы управления Windows для TB_MARKBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071858"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="fd998-104">\_Сообщение МАРКБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="fd998-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="fd998-105">Задает состояние выделения для данной кнопки в элементе управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="fd998-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd998-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd998-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd998-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd998-108">Идентификатор команды для кнопки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="fd998-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="fd998-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd998-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd998-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее новое состояние выделения.</span><span class="sxs-lookup"><span data-stu-id="fd998-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="fd998-111">Если **значение — true**, кнопка выделяется.</span><span class="sxs-lookup"><span data-stu-id="fd998-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="fd998-112">Если задано **значение false**, кнопка будет иметь состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fd998-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="fd998-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="fd998-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd998-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd998-114">Return value</span></span>

<span data-ttu-id="fd998-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fd998-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd998-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fd998-116">Requirements</span></span>



| <span data-ttu-id="fd998-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fd998-117">Requirement</span></span> | <span data-ttu-id="fd998-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fd998-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd998-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd998-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd998-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd998-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd998-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd998-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd998-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd998-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd998-123">Header</span><span class="sxs-lookup"><span data-stu-id="fd998-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd998-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd998-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

