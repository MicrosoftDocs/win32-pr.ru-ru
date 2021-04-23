---
title: Сообщение WM_DWMCOMPOSITIONCHANGED (Winuser. h)
description: Информирует все окна верхнего уровня, которые диспетчер окон рабочего стола (DWM) включены или отключены.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Сообщение WM_DWMCOMPOSITIONCHANGED диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691850"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="87d33-104">\_Сообщение ДВМКОМПОСИТИОНЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="87d33-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="87d33-105">Информирует все окна верхнего уровня, которые диспетчер окон рабочего стола (DWM) включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="87d33-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="87d33-106">Начиная с Windows 8, композиция DWM всегда включена, поэтому это сообщение не отправляется независимо от изменения видеорежима.</span><span class="sxs-lookup"><span data-stu-id="87d33-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="87d33-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="87d33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d33-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87d33-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87d33-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="87d33-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="87d33-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87d33-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87d33-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="87d33-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d33-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87d33-112">Return value</span></span>

<span data-ttu-id="87d33-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="87d33-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d33-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87d33-114">Remarks</span></span>

<span data-ttu-id="87d33-115">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="87d33-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="87d33-116">Функцию [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) можно использовать для определения текущего состояния композиции.</span><span class="sxs-lookup"><span data-stu-id="87d33-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d33-117">Требования</span><span class="sxs-lookup"><span data-stu-id="87d33-117">Requirements</span></span>



| <span data-ttu-id="87d33-118">Требование</span><span class="sxs-lookup"><span data-stu-id="87d33-118">Requirement</span></span> | <span data-ttu-id="87d33-119">Значение</span><span class="sxs-lookup"><span data-stu-id="87d33-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87d33-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87d33-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87d33-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87d33-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="87d33-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87d33-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87d33-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87d33-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="87d33-124">Header</span><span class="sxs-lookup"><span data-stu-id="87d33-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d33-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="87d33-125"><dt>Winuser.h</dt></span></span> </dl> |



 

