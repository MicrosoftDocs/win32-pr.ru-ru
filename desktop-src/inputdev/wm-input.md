---
title: Сообщение WM_INPUT (Winuser. h)
description: Отправляется в окно, которое получает необработанные входные данные. Окно получает это сообщение через функцию WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415296"
---
# <a name="wm_input-message"></a><span data-ttu-id="e2770-105">\_Входное сообщение WM</span><span class="sxs-lookup"><span data-stu-id="e2770-105">WM\_INPUT message</span></span>

<span data-ttu-id="e2770-106">Отправляется в окно, которое получает необработанные входные данные.</span><span class="sxs-lookup"><span data-stu-id="e2770-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="e2770-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e2770-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="e2770-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2770-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2770-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2770-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="e2770-110">Входной код.</span><span class="sxs-lookup"><span data-stu-id="e2770-110">The input code.</span></span> <span data-ttu-id="e2770-111">Чтобы получить это значение, используйте макрос [**Get \_ равинпут \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) .</span><span class="sxs-lookup"><span data-stu-id="e2770-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="e2770-112">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e2770-112">Can be one of the following values:</span></span>

| <span data-ttu-id="e2770-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e2770-113">Value</span></span> | <span data-ttu-id="e2770-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e2770-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="e2770-115"><dt>**RIM \_ ВХОДные данные**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2770-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e2770-116">Входные данные были выполнены, пока приложение находилось на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="e2770-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="e2770-117">Приложение должно вызвать [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы система могла выполнить очистку.</span><span class="sxs-lookup"><span data-stu-id="e2770-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="e2770-118"><dt>**RIM \_ ИНПУТСИНК**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2770-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e2770-119">Входные данные были выполнены, пока приложение не находилось на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="e2770-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="e2770-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2770-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="e2770-121">Обработчик **хравинпут** для структуры [**равинпут**](/windows/win32/api/winuser/ns-winuser-rawinput) , которая содержит необработанные данные от устройства.</span><span class="sxs-lookup"><span data-stu-id="e2770-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="e2770-122">Чтобы получить необработанные данные, используйте этот маркер в вызове [**жетравинпутдата**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span><span class="sxs-lookup"><span data-stu-id="e2770-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2770-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2770-123">Return value</span></span>

<span data-ttu-id="e2770-124">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="e2770-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2770-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2770-125">Remarks</span></span>

<span data-ttu-id="e2770-126">Необработанные входные данные доступны, только если приложение вызывает [**регистерравинпутдевицес**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) с допустимыми спецификациями устройств.</span><span class="sxs-lookup"><span data-stu-id="e2770-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2770-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e2770-127">Requirements</span></span>

| <span data-ttu-id="e2770-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e2770-128">Requirement</span></span> | <span data-ttu-id="e2770-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e2770-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="e2770-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2770-130">Minimum supported client</span></span> | <span data-ttu-id="e2770-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2770-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="e2770-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2770-132">Minimum supported server</span></span> | <span data-ttu-id="e2770-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2770-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="e2770-134">Header</span><span class="sxs-lookup"><span data-stu-id="e2770-134">Header</span></span> | <dl> <span data-ttu-id="e2770-135"><dt>**Winuser. h (включение Windows. h)**</dt></span><span class="sxs-lookup"><span data-stu-id="e2770-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e2770-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2770-136">See also</span></span>

<span data-ttu-id="e2770-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e2770-137">**Reference**</span></span>

[<span data-ttu-id="e2770-138">**жетравинпутдата**</span><span class="sxs-lookup"><span data-stu-id="e2770-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="e2770-139">**регистерравинпутдевицес**</span><span class="sxs-lookup"><span data-stu-id="e2770-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="e2770-140">**равинпут**</span><span class="sxs-lookup"><span data-stu-id="e2770-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="e2770-141">**ПОЛУЧИТЬ \_ равинпут \_ код \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="e2770-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="e2770-142">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e2770-142">**Conceptual**</span></span>

[<span data-ttu-id="e2770-143">Необработанный ввод</span><span class="sxs-lookup"><span data-stu-id="e2770-143">Raw Input</span></span>](raw-input.md)
