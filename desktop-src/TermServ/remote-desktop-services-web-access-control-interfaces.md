---
title: Интерфейсы службы удаленных рабочих столов Веб-доступ элементов управления
description: Поддерживает публикацию ресурсов для отдельных пользователей в подключения к удаленным рабочим столам и приложениям RemoteApp. Этот элемент управления является оболочкой для подключение к удаленному рабочему столу клиента (MsTscAx.dll), а также прокси-сервера среды выполнения подключений RemoteApp и Desktop Connections (Tswbprxy.exe).
ms.assetid: 69c03f60-11e0-454b-a661-e608e7ca7254
ms.tgt_platform: multiple
keywords:
- Службы удаленных рабочих столов службы удаленных рабочих столов, интерфейсы управления веб-доступом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c30f7fbf0030cd62dff221586cf4d44c90f473
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068019"
---
# <a name="remote-desktop-services-web-access-control-interfaces"></a><span data-ttu-id="2ff70-105">Интерфейсы службы удаленных рабочих столов Веб-доступ элементов управления</span><span class="sxs-lookup"><span data-stu-id="2ff70-105">Remote Desktop Services Web Access Control interfaces</span></span>

<span data-ttu-id="2ff70-106">Элемент управления Веб-доступ службы удаленных рабочих столов поддерживает публикацию пользовательских ресурсов в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2ff70-106">The Remote Desktop Services Web Access Control supports the publishing of user-specific resources in RemoteApp and Desktop Connection.</span></span> <span data-ttu-id="2ff70-107">Этот элемент управления является оболочкой для подключение к удаленному рабочему столу клиента (MsTscAx.dll), а также прокси-сервера среды выполнения подключений RemoteApp и Desktop Connections (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="2ff70-107">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ff70-108">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2ff70-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2ff70-109">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="2ff70-109">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dd>

<span data-ttu-id="2ff70-110">Отображение свойств, запускающих клиент подключение к удаленному рабочему столу из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или других веб-порталов.</span><span class="sxs-lookup"><span data-stu-id="2ff70-110">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff70-111">**имсрдпворкспаце**</span><span class="sxs-lookup"><span data-stu-id="2ff70-111">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> <dd>

<span data-ttu-id="2ff70-112">Предоставляет методы, управляющие учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2ff70-112">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="2ff70-113">**IMsRdpWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="2ff70-113">**IMsRdpWorkspace2**</span></span>](imsrdpworkspace2.md)
</dt> <dd>

<span data-ttu-id="2ff70-114">Предоставляет метод, связывающий подключения к удаленным рабочим столам и приложениям RemoteApp учетные данные с соединением.</span><span class="sxs-lookup"><span data-stu-id="2ff70-114">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span>

</dd> </dl>

 

 




