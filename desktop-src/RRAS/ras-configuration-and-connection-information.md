---
title: Сведения о конфигурации RAS и подключении
description: Приложения, работающие под управлением Windows NT 4,0 и более поздних версий и Windows 95, могут использовать функцию Расенумконнектионс для получения сведений о существующих подключениях на локальном компьютере.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Настройка и подключение, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672055"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="a62f6-104">Сведения о конфигурации RAS и подключении</span><span class="sxs-lookup"><span data-stu-id="a62f6-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="a62f6-105">Приложения, работающие под управлением Windows NT 4,0 и более поздних версий и Windows 95, могут использовать функцию [**расенумконнектионс**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) для получения сведений о существующих подключениях на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a62f6-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="a62f6-106">Сведения для каждого подключения включают в себя маркер подключения и имя записи телефонной книги, используемой для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="a62f6-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="a62f6-107">Вы можете использовать маркер соединения в вызове функции [**расжетконнектстатус**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) , чтобы получить текущее состояние соединения.</span><span class="sxs-lookup"><span data-stu-id="a62f6-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="a62f6-108">В Windows NT Server 4,0 и более поздних версиях предусмотрены две новые функции для получения сведений об RAS.</span><span class="sxs-lookup"><span data-stu-id="a62f6-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="a62f6-109">Windows 95does не поддерживает эти функции.</span><span class="sxs-lookup"><span data-stu-id="a62f6-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="a62f6-110">Функция [**расенумдевицес**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) возвращает имя и тип устройств, ПОДДЕРЖИВАЮЩИХ службу RAS, настроенных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a62f6-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="a62f6-111">Функция [**расконнектионнотификатион**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) указывает объект события, который система сообщает при создании или завершении подключения RAS.</span><span class="sxs-lookup"><span data-stu-id="a62f6-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




