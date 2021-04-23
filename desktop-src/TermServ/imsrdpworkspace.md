---
title: Интерфейс Имсрдпворкспаце
description: Предоставляет методы, управляющие учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпворкспаце
- Службы удаленных рабочих столов интерфейса Имсрдпворкспаце, описание
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988277"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="eabd6-105">Интерфейс Имсрдпворкспаце</span><span class="sxs-lookup"><span data-stu-id="eabd6-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="eabd6-106">Предоставляет методы, управляющие учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="eabd6-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="eabd6-107">Этот интерфейс реализуется элементом управления службы удаленных рабочих столов Веб-доступ.</span><span class="sxs-lookup"><span data-stu-id="eabd6-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="eabd6-108">Этот элемент управления является оболочкой для подключение к удаленному рабочему столу клиента (MsTscAx.dll), а также прокси-сервера среды выполнения подключений RemoteApp и Desktop Connections (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="eabd6-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="eabd6-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="eabd6-109">Members</span></span>

<span data-ttu-id="eabd6-110">Интерфейс **имсрдпворкспаце** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="eabd6-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eabd6-111">**Имсрдпворкспаце** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eabd6-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="eabd6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="eabd6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eabd6-113">Методы</span><span class="sxs-lookup"><span data-stu-id="eabd6-113">Methods</span></span>

<span data-ttu-id="eabd6-114">Интерфейс **имсрдпворкспаце** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="eabd6-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="eabd6-115">Метод</span><span class="sxs-lookup"><span data-stu-id="eabd6-115">Method</span></span>                                                                                   | <span data-ttu-id="eabd6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="eabd6-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eabd6-117">[**клеарворкспацекредентиал**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eabd6-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="eabd6-118">Удаляет учетные данные пользователя, связанные с указанным ИДЕНТИФИКАТОРом подключения.</span><span class="sxs-lookup"><span data-stu-id="eabd6-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="eabd6-119">[**дисконнектворкспаце**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eabd6-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="eabd6-120">Отключает все существующие соединения, связанные с указанным ИДЕНТИФИКАТОРом подключения, и удаляет соответствующие учетные данные пользователя из хранилища учетных данных.</span><span class="sxs-lookup"><span data-stu-id="eabd6-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="eabd6-121">[**исворкспацекредентиалспеЦифиед**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eabd6-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="eabd6-122">Определяет, существуют ли учетные данные пользователя для указанного идентификатора соединения.</span><span class="sxs-lookup"><span data-stu-id="eabd6-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="eabd6-123">[**исворкспацессоенаблед**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eabd6-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="eabd6-124">Определяет, включена ли поддержка единого входа (SSO) для подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="eabd6-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="eabd6-125">[**С проверкой подлинности**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eabd6-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="eabd6-126">Помечает проверку подлинности учетных данных пользователя для идентификатора подключения, а затем отображает уведомление о подключении в области уведомлений панели задач.</span><span class="sxs-lookup"><span data-stu-id="eabd6-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="eabd6-127">[**стартворкспаце**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eabd6-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="eabd6-128">Связывает учетные данные пользователя и сертификаты с ИДЕНТИФИКАТОРом подключения.</span><span class="sxs-lookup"><span data-stu-id="eabd6-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="eabd6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="eabd6-129">Requirements</span></span>



| <span data-ttu-id="eabd6-130">Требование</span><span class="sxs-lookup"><span data-stu-id="eabd6-130">Requirement</span></span> | <span data-ttu-id="eabd6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eabd6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eabd6-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eabd6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eabd6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eabd6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eabd6-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eabd6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eabd6-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eabd6-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="eabd6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eabd6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eabd6-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eabd6-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="eabd6-138">IID</span><span class="sxs-lookup"><span data-stu-id="eabd6-138">IID</span></span><br/>                      | <span data-ttu-id="eabd6-139">IID \_ имсрдпворкспаце определен как 145D0621-04CF-4FC2-A766-A81A9069CDF8</span><span class="sxs-lookup"><span data-stu-id="eabd6-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="eabd6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eabd6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eabd6-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="eabd6-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

