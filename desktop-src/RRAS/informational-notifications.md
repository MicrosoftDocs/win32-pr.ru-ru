---
title: Информационные уведомления
description: Для состояний соединения, известных как состояния выполнения, никакие действия обработчика уведомлений не требуются, если не возникает ошибка.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "104487361"
---
# <a name="informational-notifications"></a><span data-ttu-id="a41c7-103">Информационные уведомления</span><span class="sxs-lookup"><span data-stu-id="a41c7-103">Informational Notifications</span></span>

<span data-ttu-id="a41c7-104">Для [состояний соединения](connection-states.md) , известных как состояния выполнения, никакие действия обработчика уведомлений не требуются, если не возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a41c7-104">For the [connection states](connection-states.md) known as running states, no action is required of the notification handler unless an error occurs.</span></span> <span data-ttu-id="a41c7-105">Выполняемые состояния происходят во время выполнения операций подключения, которые служба RAS выполняет автоматически, например для подключения к необходимым устройствам, проверки подлинности пользователя и ожидания обратного вызова с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="a41c7-105">Running states occur during the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="a41c7-106">Уведомление — это просто отчет о состоянии клиента.</span><span class="sxs-lookup"><span data-stu-id="a41c7-106">The notification is simply a progress report to the client.</span></span>

<span data-ttu-id="a41c7-107">Клиент может передавать эти информационные уведомления пользователю.</span><span class="sxs-lookup"><span data-stu-id="a41c7-107">The client can choose to pass these informational notifications on to the user.</span></span> <span data-ttu-id="a41c7-108">В некоторых выполняющихся состояниях клиенту может потребоваться отобразить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a41c7-108">In some running states, the client may want to display additional information.</span></span> <span data-ttu-id="a41c7-109">Например, обработчик уведомлений, получающий уведомление РАСКС \_ коннектдевице, может вызвать функцию [**расжетконнектстатус**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) , чтобы получить имя и тип устройства, к которому выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="a41c7-109">For example, a notification handler that receives a RASCS\_ConnectDevice notification can call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the name and type of the device being connected to.</span></span> <span data-ttu-id="a41c7-110">Другой пример — когда клиент получает \_ запланированное уведомление раскс.</span><span class="sxs-lookup"><span data-stu-id="a41c7-110">Another example is when the client receives a RASCS\_Projected notification.</span></span> <span data-ttu-id="a41c7-111">Это происходит при завершении фазы проекции службы RAS для операции подключения.</span><span class="sxs-lookup"><span data-stu-id="a41c7-111">This occurs when the RAS projection phase of the connection operation has been completed.</span></span> <span data-ttu-id="a41c7-112">Клиент может вызвать функцию [**расжетпрожектионинфо**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) для получения дополнительных сведений о проекции.</span><span class="sxs-lookup"><span data-stu-id="a41c7-112">The client can call the [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) function to get additional information about the projection.</span></span> <span data-ttu-id="a41c7-113">Клиент может использовать эти сведения для уведомления пользователя о том, какие сетевые протоколы могут использоваться этим подключением.</span><span class="sxs-lookup"><span data-stu-id="a41c7-113">The client can use this information to notify the user as to which network protocols can be used by this connection.</span></span>

<span data-ttu-id="a41c7-114">Не следует писать код, который зависит от порядка или вхождения определенных информационных состояний, так как это может различаться для разных платформ.</span><span class="sxs-lookup"><span data-stu-id="a41c7-114">You should avoid writing code that depends on the order or occurrence of particular informational states, because this may vary between platforms.</span></span>

 

 




