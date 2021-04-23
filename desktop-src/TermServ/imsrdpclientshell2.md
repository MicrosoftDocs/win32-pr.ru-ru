---
title: Интерфейс IMsRdpClientShell2
description: Отображение свойств, запускающих клиент подключение к удаленному рабочему столу из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или других веб-порталов.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientShell2
- Службы удаленных рабочих столов интерфейса IMsRdpClientShell2, описание
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801564"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="e154d-105">Интерфейс IMsRdpClientShell2</span><span class="sxs-lookup"><span data-stu-id="e154d-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="e154d-106">Отображение свойств, запускающих клиент подключение к удаленному рабочему столу из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или других веб-порталов.</span><span class="sxs-lookup"><span data-stu-id="e154d-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="e154d-107">Этот интерфейс реализуется элементом управления службы удаленных рабочих столов Веб-доступ, который представляет собой оболочку для подключение к удаленному рабочему столу клиента (MsTscAx.dll), а также прокси-сервер среды выполнения удаленных подключений RemoteApp и Desktop Connections (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="e154d-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="e154d-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="e154d-108">Members</span></span>

<span data-ttu-id="e154d-109">Интерфейс **IMsRdpClientShell2** наследует от **имсрдпклиентшелл**.</span><span class="sxs-lookup"><span data-stu-id="e154d-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="e154d-110">**IMsRdpClientShell2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e154d-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="e154d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e154d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e154d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e154d-112">Properties</span></span>

<span data-ttu-id="e154d-113">Интерфейс **IMsRdpClientShell2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e154d-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="e154d-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="e154d-114">Property</span></span>                                                                               | <span data-ttu-id="e154d-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e154d-115">Access type</span></span>          | <span data-ttu-id="e154d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e154d-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e154d-117">**мсрдпворкспаце**</span><span class="sxs-lookup"><span data-stu-id="e154d-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="e154d-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e154d-118">Read-only</span></span><br/> | <span data-ttu-id="e154d-119">Получает указатель на интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) , используемый для управления учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e154d-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="e154d-120">**секуредсеттингсенаблед**</span><span class="sxs-lookup"><span data-stu-id="e154d-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="e154d-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e154d-121">Read-only</span></span><br/> | <span data-ttu-id="e154d-122">Получает значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e154d-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="e154d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e154d-123">Requirements</span></span>



| <span data-ttu-id="e154d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e154d-124">Requirement</span></span> | <span data-ttu-id="e154d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e154d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e154d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e154d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e154d-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e154d-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e154d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e154d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e154d-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e154d-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="e154d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e154d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e154d-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e154d-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e154d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e154d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e154d-133">**имсрдпворкспаце**</span><span class="sxs-lookup"><span data-stu-id="e154d-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





