---
title: Интерфейсы среды выполнения подключения к удаленным рабочим столам и приложениям RemoteApp
description: Поддерживает интерфейсы, позволяющие разрабатывать пользовательские клиенты в подключения к удаленным рабочим столам и приложениям RemoteApp.
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- Справочник по API среды выполнения подключения к удаленным рабочим столам и приложениям RemoteApp службы удаленных рабочих столов службы удаленных рабочих столов
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133174"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="8f968-104">Интерфейсы среды выполнения подключения к удаленным рабочим столам и приложениям RemoteApp</span><span class="sxs-lookup"><span data-stu-id="8f968-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="8f968-105">API среды выполнения подключения к удаленным рабочим столам и приложениям RemoteApp поддерживает интерфейсы, позволяющие разрабатывать пользовательские клиенты в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8f968-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="8f968-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="8f968-107">**иворкспаце**</span><span class="sxs-lookup"><span data-stu-id="8f968-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="8f968-108">Предоставляет методы, предоставляющие сведения о соединении в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="8f968-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="8f968-110">Предоставляет дополнительные методы, предоставляющие сведения о соединении в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="8f968-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="8f968-112">Предоставляет методы, предоставляющие сведения о соединении в подключения к удаленным рабочим столам и приложениям RemoteApp, и добавляет возможность извлечения или установки токена утверждений.</span><span class="sxs-lookup"><span data-stu-id="8f968-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-113">**иворкспацеклиентекст**</span><span class="sxs-lookup"><span data-stu-id="8f968-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="8f968-114">Предоставляет методы, позволяющие среде выполнения отключать пользовательский клиент в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-115">**иворкспацерегистратион**</span><span class="sxs-lookup"><span data-stu-id="8f968-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="8f968-116">Предоставляет методы, добавляющие и удаляющие ссылки на пользовательские клиенты в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="8f968-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="8f968-118">Предоставляет методы, добавляющие и удаляющие ссылки на пользовательские клиенты в подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-119">**иворкспацерепортмессаже**</span><span class="sxs-lookup"><span data-stu-id="8f968-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="8f968-120">Предоставляет методы, поддерживающие обработку сообщений об ошибках для удаленных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="8f968-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-121">**иворкспацерестиперегистри**</span><span class="sxs-lookup"><span data-stu-id="8f968-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="8f968-122">Предоставляет методы, позволяющие подключаемому модулю управлять расширениями имен файлов сторонних производителей в среде выполнения подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-123">**иворкспацескриптабле**</span><span class="sxs-lookup"><span data-stu-id="8f968-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="8f968-124">Предоставляет методы, управляющие учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="8f968-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="8f968-126">Предоставляет методы, управляющие учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="8f968-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="8f968-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="8f968-128">Предоставляет методы, управляющие учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f968-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




