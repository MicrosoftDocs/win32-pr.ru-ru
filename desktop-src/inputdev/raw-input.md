---
title: Необработанный ввод
description: В этом разделе описывается, как система предоставляет приложению необработанные входные данные и как приложение получает и обрабатывает эти входные данные.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Пользовательский интерфейс Windows, ввод данных пользователем
- Пользовательский интерфейс Windows, необработанный ввод
- Ввод данных пользователем, необработанный ввод
- запись вводимых пользователем данных, необработанные входные данные
- необработанный ввод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412890"
---
# <a name="raw-input"></a><span data-ttu-id="dd5fa-108">Необработанный ввод</span><span class="sxs-lookup"><span data-stu-id="dd5fa-108">Raw Input</span></span>

<span data-ttu-id="dd5fa-109">В этом разделе описывается, как система предоставляет приложению необработанные входные данные и как приложение получает и обрабатывает эти входные данные.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="dd5fa-110">Необработанные входные данные иногда называются универсальными входными данными.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="dd5fa-111">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="dd5fa-111">In This Section</span></span>



| <span data-ttu-id="dd5fa-112">Имя</span><span class="sxs-lookup"><span data-stu-id="dd5fa-112">Name</span></span>                                           | <span data-ttu-id="dd5fa-113">Описание</span><span class="sxs-lookup"><span data-stu-id="dd5fa-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd5fa-114">О необработанном вводе</span><span class="sxs-lookup"><span data-stu-id="dd5fa-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="dd5fa-115">Обсуждаются пользовательские данные с устройств, таких как джойстики, сенсорные экраны и микрофоны.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="dd5fa-116">Использование необработанных входных данных</span><span class="sxs-lookup"><span data-stu-id="dd5fa-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="dd5fa-117">Содержит образец кода для задач, связанных с необработанными входными данными.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="dd5fa-118">Справочник по необработанным входным данным</span><span class="sxs-lookup"><span data-stu-id="dd5fa-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="dd5fa-119">Содержит справочник по API.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="dd5fa-120">Функции</span><span class="sxs-lookup"><span data-stu-id="dd5fa-120">Functions</span></span>



| <span data-ttu-id="dd5fa-121">Имя</span><span class="sxs-lookup"><span data-stu-id="dd5fa-121">Name</span></span>                                                                 | <span data-ttu-id="dd5fa-122">Описание</span><span class="sxs-lookup"><span data-stu-id="dd5fa-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd5fa-123">**дефравинпутпрок**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="dd5fa-124">Вызывает необработанную входную процедуру по умолчанию, чтобы обеспечить обработку по умолчанию для любых необработанных входных сообщений, которые приложение не обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="dd5fa-125">Эта функция гарантирует, что каждое сообщение будет обработано.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="dd5fa-126">[**Дефравинпутпрок**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) вызывается с теми же параметрами, которые были получены процедурой окна.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="dd5fa-127">**жетравинпутбуффер**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="dd5fa-128">Выполняет буферизованное чтение необработанных входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="dd5fa-129">**жетравинпутдата**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="dd5fa-130">Возвращает необработанный ввод с указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="dd5fa-131">**жетравинпутдевицеинфо**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="dd5fa-132">Возвращает сведения о необработанном устройстве ввода.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="dd5fa-133">**жетравинпутдевицелист**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="dd5fa-134">Перечисляет необработанные входные устройства, подключенные к системе.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="dd5fa-135">**жетрегистередравинпутдевицес**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="dd5fa-136">Возвращает сведения о необработанных устройствах ввода для текущего приложения.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="dd5fa-137">**регистерравинпутдевицес**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="dd5fa-138">Регистрирует устройства, которые предоставляют необработанные входные данные.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="dd5fa-139">Макросы</span><span class="sxs-lookup"><span data-stu-id="dd5fa-139">Macros</span></span>



| <span data-ttu-id="dd5fa-140">Имя</span><span class="sxs-lookup"><span data-stu-id="dd5fa-140">Name</span></span>                                                            | <span data-ttu-id="dd5fa-141">Описание</span><span class="sxs-lookup"><span data-stu-id="dd5fa-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd5fa-142">**ПОЛУЧИТЬ \_ равинпут \_ код \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="dd5fa-143">Получает входной код из аргумента *wParam* в [**\_ входных данных WM**](wm-input.md).</span><span class="sxs-lookup"><span data-stu-id="dd5fa-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="dd5fa-144">**некстравинпутблокк**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="dd5fa-145">Возвращает расположение следующей структуры в массиве структур [**равинпут**](/windows/win32/api/winuser/ns-winuser-rawinput) .</span><span class="sxs-lookup"><span data-stu-id="dd5fa-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="dd5fa-146">Уведомления</span><span class="sxs-lookup"><span data-stu-id="dd5fa-146">Notifications</span></span>



| <span data-ttu-id="dd5fa-147">Имя</span><span class="sxs-lookup"><span data-stu-id="dd5fa-147">Name</span></span>                                                        | <span data-ttu-id="dd5fa-148">Описание</span><span class="sxs-lookup"><span data-stu-id="dd5fa-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="dd5fa-149">**\_входные данные WM**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="dd5fa-150">Отправляется в окно, которое получает необработанные входные данные.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="dd5fa-151">**\_изменение входного \_ устройства WM \_**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="dd5fa-152">Отправляется в окно, зарегистрированное для получения необработанных входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="dd5fa-153">Структуры</span><span class="sxs-lookup"><span data-stu-id="dd5fa-153">Structures</span></span>



| <span data-ttu-id="dd5fa-154">Имя</span><span class="sxs-lookup"><span data-stu-id="dd5fa-154">Name</span></span>                                                            | <span data-ttu-id="dd5fa-155">Описание</span><span class="sxs-lookup"><span data-stu-id="dd5fa-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd5fa-156">**равхид**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="dd5fa-157">Описывает формат необработанных входных данных из устройство HID (HID).</span><span class="sxs-lookup"><span data-stu-id="dd5fa-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="dd5fa-158">**равинпут**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="dd5fa-159">Содержит необработанные данные ввода с устройства.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="dd5fa-160">**равинпутдевице**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="dd5fa-161">Определяет сведения для необработанных входных устройств.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="dd5fa-162">**равинпутдевицелист**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="dd5fa-163">Содержит сведения о необработанном устройстве ввода.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="dd5fa-164">**равинпусеадер**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="dd5fa-165">Содержит сведения о заголовке, которые являются частью необработанных входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="dd5fa-166">**равкэйбоард**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="dd5fa-167">Содержит сведения о состоянии клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="dd5fa-168">**равмаусе**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="dd5fa-169">Содержит сведения о состоянии мыши.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="dd5fa-170">**\_ \_ сведения об устройстве RID**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="dd5fa-171">Определяет необработанные входные данные, поступающие с любого устройства.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="dd5fa-172">**\_ \_ сведения об устройстве RID \_ HID**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="dd5fa-173">Определяет необработанные входные данные, поступающие из указанного HID.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="dd5fa-174">**\_Клавиатура " \_ сведения об устройстве RID" \_**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="dd5fa-175">Определяет необработанные входные данные, поступающие с указанной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="dd5fa-176">**\_указатель на \_ сведения об устройстве RID \_**</span><span class="sxs-lookup"><span data-stu-id="dd5fa-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="dd5fa-177">Определяет необработанные входные данные, поступающие от указанной мыши.</span><span class="sxs-lookup"><span data-stu-id="dd5fa-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

