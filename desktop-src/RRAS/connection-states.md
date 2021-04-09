---
title: Состояния соединения
description: Во время подключения к удаленному серверу диспетчер подключений удаленного доступа и сервер RAS на удаленном компьютере выполняют несколько шагов для установки соединения.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890865"
---
# <a name="connection-states"></a><span data-ttu-id="fd531-103">Состояния соединения</span><span class="sxs-lookup"><span data-stu-id="fd531-103">Connection States</span></span>

<span data-ttu-id="fd531-104">Во время подключения к удаленному серверу диспетчер подключений удаленного доступа и сервер RAS на удаленном компьютере выполняют несколько шагов для установки соединения.</span><span class="sxs-lookup"><span data-stu-id="fd531-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="fd531-105">Каждое из этих действий определяется состоянием соединения.</span><span class="sxs-lookup"><span data-stu-id="fd531-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="fd531-106">Перечисление [**расконнстате**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) представляет собой набор значений, соответствующих этим состояниям соединения.</span><span class="sxs-lookup"><span data-stu-id="fd531-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="fd531-107">Состояния подключения можно разделить на следующие три группы:</span><span class="sxs-lookup"><span data-stu-id="fd531-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="fd531-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Выполняемые состояния</span><span class="sxs-lookup"><span data-stu-id="fd531-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="fd531-109">Состояния выполнения — это часть операции подключения, которая автоматически обрабатывается службой RAS, например подключение к необходимым устройствам, проверка подлинности пользователя и ожидание обратного вызова от удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="fd531-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="fd531-110">Если ошибка не возникает, клиенту RAS не нужно предпринимать никаких действий, кроме передачи уведомления пользователю.</span><span class="sxs-lookup"><span data-stu-id="fd531-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="fd531-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Приостановленные состояния</span><span class="sxs-lookup"><span data-stu-id="fd531-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="fd531-112">[Приостановленные состояния](paused-states.md) возникают, когда удаленный сервер приостанавливает операцию подключения для получения дополнительных входных данных от пользователя.</span><span class="sxs-lookup"><span data-stu-id="fd531-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="fd531-113">Во время приостановленного состояния пользователь может ввести номер [обратного вызова](callback-connections.md) , другое имя пользователя и пароль в случае сбоя проверки подлинности пользователя или новый пароль, если срок действия старого пароля истек.</span><span class="sxs-lookup"><span data-stu-id="fd531-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="fd531-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Состояния терминала</span><span class="sxs-lookup"><span data-stu-id="fd531-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="fd531-115">Состояние терминала возникает, когда соединение установлено успешно, операция подключения завершилась сбоем или соединение разорвано вызовом [**рашангуп**](/windows/desktop/api/Ras/nf-ras-rashangupa) .</span><span class="sxs-lookup"><span data-stu-id="fd531-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="fd531-116">Существует несколько механизмов, которые клиент RAS может использовать для определения текущего состояния операции подключения.</span><span class="sxs-lookup"><span data-stu-id="fd531-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="fd531-117">Когда клиент RAS выполняет функцию [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) асинхронно, диспетчер подключений удаленного доступа отправляет уведомления о ходе выполнения в [обработчик уведомлений](notification-handlers.md) клиента при каждом изменении состояния соединения.</span><span class="sxs-lookup"><span data-stu-id="fd531-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="fd531-118">Кроме того, клиент может использовать функцию [**расжетконнектстатус**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) для получения текущего состояния любой операции подключения RAS.</span><span class="sxs-lookup"><span data-stu-id="fd531-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 