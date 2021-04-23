---
description: Диспетчер синхронизации включает в себя компоненты пользовательского интерфейса, такие как диалоговые окна с вкладками в службе Синкмгр, диалоговые окна ошибок и диалоги хода выполнения.
title: Архитектура диспетчера синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819033"
---
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="d0370-103">Архитектура диспетчера синхронизации</span><span class="sxs-lookup"><span data-stu-id="d0370-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="d0370-104">Диспетчер синхронизации включает в себя компоненты пользовательского интерфейса, такие как диалоговые окна с вкладками в службе Синкмгр, диалоговые окна ошибок и диалоги хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d0370-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="d0370-105">С помощью компонентов пользовательского интерфейса конечный пользователь может запланировать синхронизацию приложений и настроить автоматическую синхронизацию в сочетании с указанными системными событиями.</span><span class="sxs-lookup"><span data-stu-id="d0370-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="d0370-106">Например, Синкмгр может вызываться при входе пользователя в систему или при завершении работы системы.</span><span class="sxs-lookup"><span data-stu-id="d0370-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="d0370-107">Пользователь также может вызвать синхронизацию вручную.</span><span class="sxs-lookup"><span data-stu-id="d0370-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="d0370-108">Пользователь выбирает приложение и указывает элементы в приложении для синхронизации и задает событие триггера.</span><span class="sxs-lookup"><span data-stu-id="d0370-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="d0370-109">Например, в приложении электронной почты папка «Входящие», «исходящие» или другие папки, содержащие сообщения, может быть отдельным элементом для приложения.</span><span class="sxs-lookup"><span data-stu-id="d0370-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="d0370-110">Синкмгр также включает программный интерфейс, чтобы приложения могли регистрироваться для использования функций синхронизации, могут обрабатывать ошибки и получать сведения о ходе выполнения и уведомления в процессе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d0370-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



