---
title: Сетевые операции Windows
description: Приложение может использовать функции Внет для просмотра, добавления или отмены сетевых подключений в любом месте иерархии сети.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337921"
---
# <a name="windows-networking-operations"></a><span data-ttu-id="c0b33-103">Сетевые операции Windows</span><span class="sxs-lookup"><span data-stu-id="c0b33-103">Windows Networking Operations</span></span>

<span data-ttu-id="c0b33-104">Приложение может использовать функции Внет для просмотра, добавления или отмены сетевых подключений в любом месте иерархии сети.</span><span class="sxs-lookup"><span data-stu-id="c0b33-104">An application can use the WNet functions to browse, add, or cancel network connections anywhere in the network hierarchy.</span></span>

<span data-ttu-id="c0b33-105">*Постоянное подключение* — это сетевое подключение, которое система автоматически восстанавливает при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="c0b33-105">A *persistent connection* is a network connection that the system automatically restores when the user logs on.</span></span> <span data-ttu-id="c0b33-106">Вы можете вызвать функции [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (или [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) и [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , чтобы управлять тем, является ли сетевое подключение постоянным от одного сеанса к другому.</span><span class="sxs-lookup"><span data-stu-id="c0b33-106">You can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) functions to control whether a network connection is persistent from one session to the next.</span></span>

<span data-ttu-id="c0b33-107">Чтобы найти имя пользователя по умолчанию или имя пользователя, используемое для установления сетевого подключения, вызовите функцию [**внетжетусер**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="c0b33-107">To find the default user name or the user name used to establish a network connection, call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="c0b33-108">Помимо вызова функций Внет, процесс также может использовать маилслотс и именованные каналы для взаимодействия с другим процессом.</span><span class="sxs-lookup"><span data-stu-id="c0b33-108">In addition to calling the WNet functions, a process can also use mailslots and named pipes to communicate with another process.</span></span> <span data-ttu-id="c0b33-109">Дополнительные сведения см. в разделе [маилслотс](/windows/desktop/ipc/mailslots) и [каналы](/windows/desktop/ipc/pipes).</span><span class="sxs-lookup"><span data-stu-id="c0b33-109">For more information, see [Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).</span></span>

 

 