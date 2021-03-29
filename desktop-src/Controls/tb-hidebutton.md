---
title: Сообщение TB_HIDEBUTTON (Коммктрл. h)
description: Скрывает или отображает указанную кнопку на панели инструментов.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- Элементы управления Windows для TB_HIDEBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988475"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="73534-104">\_Сообщение ХИДЕБУТТОН ТБ</span><span class="sxs-lookup"><span data-stu-id="73534-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="73534-105">Скрывает или отображает указанную кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="73534-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="73534-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73534-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73534-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73534-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73534-108">Идентификатор команды для скрытия или отображения.</span><span class="sxs-lookup"><span data-stu-id="73534-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="73534-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73534-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73534-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли скрывать или отображать указанную кнопку.</span><span class="sxs-lookup"><span data-stu-id="73534-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="73534-111">Если **значение равно true**, кнопка скрыта.</span><span class="sxs-lookup"><span data-stu-id="73534-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="73534-112">Если задано **значение false**, отображается кнопка.</span><span class="sxs-lookup"><span data-stu-id="73534-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="73534-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="73534-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73534-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73534-114">Return value</span></span>

<span data-ttu-id="73534-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="73534-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="73534-116">Требования</span><span class="sxs-lookup"><span data-stu-id="73534-116">Requirements</span></span>



| <span data-ttu-id="73534-117">Требование</span><span class="sxs-lookup"><span data-stu-id="73534-117">Requirement</span></span> | <span data-ttu-id="73534-118">Значение</span><span class="sxs-lookup"><span data-stu-id="73534-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73534-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73534-119">Minimum supported client</span></span><br/> | <span data-ttu-id="73534-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73534-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73534-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73534-121">Minimum supported server</span></span><br/> | <span data-ttu-id="73534-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73534-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73534-123">Header</span><span class="sxs-lookup"><span data-stu-id="73534-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="73534-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="73534-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

