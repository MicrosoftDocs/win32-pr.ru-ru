---
title: Сообщение WM_INPUT_DEVICE_CHANGE (Winuser. h)
description: Отправляется в окно, зарегистрированное для получения необработанных входных данных. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "104070797"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="5afdc-105">Сообщение WM_INPUT_DEVICE_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5afdc-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="5afdc-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5afdc-106">Description</span></span>

<span data-ttu-id="5afdc-107">Отправляется в окно, зарегистрированное для получения необработанных входных данных.</span><span class="sxs-lookup"><span data-stu-id="5afdc-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="5afdc-108">Необработанные входные уведомления доступны только после того, как приложение вызывает [регистерравинпутдевицес](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) с флагом [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) .</span><span class="sxs-lookup"><span data-stu-id="5afdc-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="5afdc-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5afdc-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="5afdc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5afdc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5afdc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5afdc-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="5afdc-112">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="5afdc-112">Type: **WPARAM**</span></span>

<span data-ttu-id="5afdc-113">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="5afdc-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="5afdc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5afdc-114">Value</span></span>                    | <span data-ttu-id="5afdc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5afdc-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="5afdc-116">**\_прибытие гидк**</span><span class="sxs-lookup"><span data-stu-id="5afdc-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="5afdc-117">1</span><span class="sxs-lookup"><span data-stu-id="5afdc-117">1</span></span> | <span data-ttu-id="5afdc-118">В систему Добавлено новое устройство.</span><span class="sxs-lookup"><span data-stu-id="5afdc-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="5afdc-119">Чтобы получить дополнительные сведения об устройстве, можно вызвать [жетравинпутдевицеинфо](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5afdc-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="5afdc-120">**\_Удаление гидк**</span><span class="sxs-lookup"><span data-stu-id="5afdc-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="5afdc-121">2</span><span class="sxs-lookup"><span data-stu-id="5afdc-121">2</span></span> | <span data-ttu-id="5afdc-122">Устройство было удалено из системы.</span><span class="sxs-lookup"><span data-stu-id="5afdc-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="5afdc-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5afdc-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="5afdc-124">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="5afdc-124">Type: **LPARAM**</span></span>

<span data-ttu-id="5afdc-125">**Обработчик** необработанного входного устройства.</span><span class="sxs-lookup"><span data-stu-id="5afdc-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5afdc-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5afdc-126">Return value</span></span>

<span data-ttu-id="5afdc-127">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="5afdc-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="5afdc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5afdc-128">See also</span></span>

<span data-ttu-id="5afdc-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5afdc-129">**Conceptual**</span></span>

[<span data-ttu-id="5afdc-130">Необработанный ввод</span><span class="sxs-lookup"><span data-stu-id="5afdc-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="5afdc-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5afdc-131">**Reference**</span></span>

[<span data-ttu-id="5afdc-132">регистерравинпутдевицес</span><span class="sxs-lookup"><span data-stu-id="5afdc-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="5afdc-133">Структура РАВИНПУТДЕВИЦЕ</span><span class="sxs-lookup"><span data-stu-id="5afdc-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

