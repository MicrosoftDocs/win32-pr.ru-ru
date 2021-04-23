---
title: Интерфейс Иремотедесктопклиентевентс
description: Предоставляет методы, получающие от сервера сведения, связанные с событиями клиентского элемента управления.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, описание
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071627"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="265df-105">Интерфейс Иремотедесктопклиентевентс</span><span class="sxs-lookup"><span data-stu-id="265df-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="265df-106">Предоставляет методы, получающие от сервера сведения, связанные с событиями клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="265df-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="265df-107">К событиям относятся подключение и отключение, запросы в полноэкранном режиме, успешный вход и условия ошибки.</span><span class="sxs-lookup"><span data-stu-id="265df-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="265df-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="265df-108">Members</span></span>

<span data-ttu-id="265df-109">Интерфейс **иремотедесктопклиентевентс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="265df-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="265df-110">**Иремотедесктопклиентевентс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="265df-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="265df-111">Методы</span><span class="sxs-lookup"><span data-stu-id="265df-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="265df-112">Методы</span><span class="sxs-lookup"><span data-stu-id="265df-112">Methods</span></span>

<span data-ttu-id="265df-113">Интерфейс **иремотедесктопклиентевентс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="265df-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="265df-114">Метод</span><span class="sxs-lookup"><span data-stu-id="265df-114">Method</span></span>                                                                                      | <span data-ttu-id="265df-115">Описание</span><span class="sxs-lookup"><span data-stu-id="265df-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="265df-116">**онадминмессажерецеивед**</span><span class="sxs-lookup"><span data-stu-id="265df-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="265df-117">Вызывается, когда клиентский элемент управления получает административное сообщение.</span><span class="sxs-lookup"><span data-stu-id="265df-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="265df-118">**онаутореконнектед**</span><span class="sxs-lookup"><span data-stu-id="265df-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="265df-119">Вызывается при автоматическом повторном подключении клиентского элемента управления к удаленному сеансу.</span><span class="sxs-lookup"><span data-stu-id="265df-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="265df-120">**онаутореконнектинг**</span><span class="sxs-lookup"><span data-stu-id="265df-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="265df-121">Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="265df-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="265df-122">**Подключено**</span><span class="sxs-lookup"><span data-stu-id="265df-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="265df-123">Вызывается, когда клиентский элемент управления подключается к удаленному сеансу.</span><span class="sxs-lookup"><span data-stu-id="265df-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="265df-124">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="265df-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="265df-125">Вызывается, когда клиентский элемент управления пытается установить соединение с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="265df-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="265df-126">**ондиалогдисмиссед**</span><span class="sxs-lookup"><span data-stu-id="265df-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="265df-127">Вызывается после закрытия диалогового окна, отображаемого клиентским элементом управления.</span><span class="sxs-lookup"><span data-stu-id="265df-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="265df-128">**ондиалогдисплайинг**</span><span class="sxs-lookup"><span data-stu-id="265df-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="265df-129">Вызывается до того, как элемент управления выводит диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="265df-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="265df-130">**С отключением**</span><span class="sxs-lookup"><span data-stu-id="265df-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="265df-131">Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса.</span><span class="sxs-lookup"><span data-stu-id="265df-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="265df-132">**онкэйкомбинатионпрессед**</span><span class="sxs-lookup"><span data-stu-id="265df-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="265df-133">Вызывается при нажатии специальных сочетаний клавиш в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="265df-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="265df-134">**онлогинкомплетед**</span><span class="sxs-lookup"><span data-stu-id="265df-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="265df-135">Вызывается, когда клиентский элемент управления успешно вошел в удаленный сеанс.</span><span class="sxs-lookup"><span data-stu-id="265df-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="265df-136">**оннетворкстатусчанжед**</span><span class="sxs-lookup"><span data-stu-id="265df-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="265df-137">Вызывается при изменении состояния сети.</span><span class="sxs-lookup"><span data-stu-id="265df-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="265df-138">**онремотедесктопсизечанжед**</span><span class="sxs-lookup"><span data-stu-id="265df-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="265df-139">Вызывается при изменении размера удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="265df-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="265df-140">**онстатусчанжед**</span><span class="sxs-lookup"><span data-stu-id="265df-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="265df-141">Вызывается, когда клиентский элемент управления обновил свое состояние.</span><span class="sxs-lookup"><span data-stu-id="265df-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="265df-142">**онтаучпоинтеркурсормовед**</span><span class="sxs-lookup"><span data-stu-id="265df-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="265df-143">Вызывается, когда курсор сенсорного указателя переместился и свойство [**евентсенаблед**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="265df-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="265df-144">Требования</span><span class="sxs-lookup"><span data-stu-id="265df-144">Requirements</span></span>



| <span data-ttu-id="265df-145">Требование</span><span class="sxs-lookup"><span data-stu-id="265df-145">Requirement</span></span> | <span data-ttu-id="265df-146">Значение</span><span class="sxs-lookup"><span data-stu-id="265df-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265df-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="265df-147">Minimum supported client</span></span><br/> | <span data-ttu-id="265df-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="265df-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="265df-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="265df-149">Minimum supported server</span></span><br/> | <span data-ttu-id="265df-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="265df-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="265df-151">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="265df-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="265df-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265df-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="265df-153">DLL</span><span class="sxs-lookup"><span data-stu-id="265df-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="265df-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265df-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="265df-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="265df-155">CLSID</span></span><br/>                    | <span data-ttu-id="265df-156">\_РЕМОТЕДЕСКТОПКЛИЕНТ CLSID определен как EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="265df-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="265df-157">IID</span><span class="sxs-lookup"><span data-stu-id="265df-157">IID</span></span><br/>                      | <span data-ttu-id="265df-158">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="265df-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="265df-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="265df-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="265df-160">Справочник по элементу управления ActiveX удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="265df-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

