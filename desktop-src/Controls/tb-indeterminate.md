---
title: Сообщение TB_INDETERMINATE (Коммктрл. h)
description: Задает или очищает неопределенное состояние указанной кнопки на панели инструментов.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- Элементы управления Windows для TB_INDETERMINATE сообщений
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071449"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="cd69a-104">\_Неопределенное сообщение ТБ</span><span class="sxs-lookup"><span data-stu-id="cd69a-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="cd69a-105">Задает или очищает неопределенное состояние указанной кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="cd69a-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd69a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd69a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd69a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd69a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd69a-108">Идентификатор команды, неопределенное состояние которой необходимо установить или удалить.</span><span class="sxs-lookup"><span data-stu-id="cd69a-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="cd69a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd69a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd69a-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли устанавливать или очищать неопределенное состояние.</span><span class="sxs-lookup"><span data-stu-id="cd69a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="cd69a-111">При **значении true** задается неопределенное состояние.</span><span class="sxs-lookup"><span data-stu-id="cd69a-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="cd69a-112">Если **значение равно false**, состояние снимается.</span><span class="sxs-lookup"><span data-stu-id="cd69a-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="cd69a-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="cd69a-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd69a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd69a-114">Return value</span></span>

<span data-ttu-id="cd69a-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cd69a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd69a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cd69a-116">Requirements</span></span>



| <span data-ttu-id="cd69a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cd69a-117">Requirement</span></span> | <span data-ttu-id="cd69a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cd69a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd69a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd69a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cd69a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd69a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd69a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd69a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cd69a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd69a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd69a-123">Header</span><span class="sxs-lookup"><span data-stu-id="cd69a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd69a-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd69a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

