---
title: Интерфейс IMsRdpWorkspace2
description: Предоставляет метод, связывающий подключения к удаленным рабочим столам и приложениям RemoteApp учетные данные с соединением.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071551"
---
# <a name="imsrdpworkspace2-interface"></a><span data-ttu-id="1a235-105">Интерфейс IMsRdpWorkspace2</span><span class="sxs-lookup"><span data-stu-id="1a235-105">IMsRdpWorkspace2 interface</span></span>

<span data-ttu-id="1a235-106">Предоставляет метод, связывающий подключения к удаленным рабочим столам и приложениям RemoteApp учетные данные с соединением.</span><span class="sxs-lookup"><span data-stu-id="1a235-106">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span> <span data-ttu-id="1a235-107">Этот интерфейс реализуется элементом управления службы удаленных рабочих столов Веб-доступ.</span><span class="sxs-lookup"><span data-stu-id="1a235-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="1a235-108">Этот элемент управления является оболочкой для подключение к удаленному рабочему столу клиента (MsTscAx.dll), а также прокси-сервера среды выполнения подключений RemoteApp и Desktop Connections (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="1a235-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="1a235-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="1a235-109">Members</span></span>

<span data-ttu-id="1a235-110">Интерфейс **имсрдпворкспаце** наследует от [**имсрдпворкспаце**](imsrdpworkspace.md).</span><span class="sxs-lookup"><span data-stu-id="1a235-110">The **IMsRdpWorkspace** interface inherits from [**IMsRdpWorkspace**](imsrdpworkspace.md).</span></span> <span data-ttu-id="1a235-111">**IMsRdpWorkspace2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1a235-111">**IMsRdpWorkspace2** also has these types of members:</span></span>

-   [<span data-ttu-id="1a235-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1a235-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1a235-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1a235-113">Methods</span></span>

<span data-ttu-id="1a235-114">Интерфейс **имсрдпворкспаце** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1a235-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="1a235-115">Метод</span><span class="sxs-lookup"><span data-stu-id="1a235-115">Method</span></span>                                                        | <span data-ttu-id="1a235-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1a235-116">Description</span></span>                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="1a235-117">[**стартворкспацеекс**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a235-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span></span> | <span data-ttu-id="1a235-118">Связывает учетные данные пользователя и сертификаты с ИДЕНТИФИКАТОРом подключения.</span><span class="sxs-lookup"><span data-stu-id="1a235-118">Associates user credentials and certificates with a connection ID.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a235-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1a235-119">Requirements</span></span>



| <span data-ttu-id="1a235-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1a235-120">Requirement</span></span> | <span data-ttu-id="1a235-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1a235-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a235-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a235-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1a235-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1a235-123">Windows 8</span></span><br/>                                                                          |
| <span data-ttu-id="1a235-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a235-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1a235-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a235-125">Windows Server 2012</span></span><br/>                                                                |
| <span data-ttu-id="1a235-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1a235-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a235-127"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a235-127"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="1a235-128">IID</span><span class="sxs-lookup"><span data-stu-id="1a235-128">IID</span></span><br/>                      | <span data-ttu-id="1a235-129">IID \_ IMsRdpWorkspace2 определен как 145D0622-04CF-4FC3-A776-A82A9169CDF8</span><span class="sxs-lookup"><span data-stu-id="1a235-129">IID\_IMsRdpWorkspace2 is defined as 145D0622-04CF-4FC3-A776-A82A9169CDF8</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1a235-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a235-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a235-131">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="1a235-131">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dt>

[<span data-ttu-id="1a235-132">**имсрдпворкспаце**</span><span class="sxs-lookup"><span data-stu-id="1a235-132">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

