---
title: Рекомендации по периферийным устройствам
description: Если устройство оборудования не предназначено для работы в удаленном сеансе, поставщики должны убедиться, что программное обеспечение драйвера устройства принудительно отключает перенаправление устройства, используя системную политику или групповую политику.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411190"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="2a576-103">Рекомендации по периферийным устройствам</span><span class="sxs-lookup"><span data-stu-id="2a576-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="2a576-104">Для клиента подключение к удаленному рабочему столу (RDC) сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) является локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="2a576-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="2a576-105">Следовательно, такие устройства, как диски и принтеры, подключенные к серверу, отображаются как локальные устройства для клиента.</span><span class="sxs-lookup"><span data-stu-id="2a576-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="2a576-106">В отличие от этого, диски и принтеры, подключенные к клиентскому терминалу, могут выглядеть как удаленные устройства в зависимости от параметров, выбранных для подключения, используемого сервера и версии используемого клиентского программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2a576-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="2a576-107">В то время как первоначальный выпуск службы удаленных рабочих столов не поддерживал приложения, отправляющие выходные данные непосредственно в последовательные, параллельные и звуковые порты, подключенные к клиентскому терминалу, текущие версии позволяют этим устройствам отображаться как локальные устройства для приложений, выполняющихся в сеансе службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="2a576-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="2a576-108">Если устройство оборудования не предназначено для работы в удаленном сеансе, поставщики должны убедиться, что программное обеспечение драйвера устройства принудительно отключает перенаправление устройства, используя системную политику или групповую политику.</span><span class="sxs-lookup"><span data-stu-id="2a576-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




