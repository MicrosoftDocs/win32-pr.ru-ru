---
title: Сообщение TB_SETSTATE (Коммктрл. h)
description: Задает состояние указанной кнопки на панели инструментов.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- Элементы управления Windows для TB_SETSTATE сообщений
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137838"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="7dfdb-104">\_Сообщение SETSTATE ТБ</span><span class="sxs-lookup"><span data-stu-id="7dfdb-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="7dfdb-105">Задает состояние указанной кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7dfdb-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dfdb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dfdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dfdb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7dfdb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dfdb-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="7dfdb-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="7dfdb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dfdb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dfdb-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) представляет собой сочетание значений, перечисленных в поле [состояния кнопки на панели инструментов](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="7dfdb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="7dfdb-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="7dfdb-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dfdb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dfdb-112">Return value</span></span>

<span data-ttu-id="7dfdb-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7dfdb-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dfdb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7dfdb-114">Requirements</span></span>



| <span data-ttu-id="7dfdb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7dfdb-115">Requirement</span></span> | <span data-ttu-id="7dfdb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7dfdb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dfdb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dfdb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7dfdb-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dfdb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dfdb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dfdb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7dfdb-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7dfdb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dfdb-121">Header</span><span class="sxs-lookup"><span data-stu-id="7dfdb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dfdb-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dfdb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

