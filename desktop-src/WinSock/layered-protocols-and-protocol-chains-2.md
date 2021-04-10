---
description: 'Сокеты Windows 2 содержат концепцию многоуровневого протокола: один, который реализует только функции обмена данными более высокого уровня, и полагается на базовый стек транспорта для фактического обмена данными с удаленной конечной точкой.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Многоуровневые протоколы и цепочки протоколов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145022"
---
# <a name="layered-protocols-and-protocol-chains"></a><span data-ttu-id="ad7e9-103">Многоуровневые протоколы и цепочки протоколов</span><span class="sxs-lookup"><span data-stu-id="ad7e9-103">Layered Protocols and Protocol Chains</span></span>

<span data-ttu-id="ad7e9-104">Сокеты Windows 2 содержат концепцию многоуровневого протокола: один, который реализует только функции обмена данными более высокого уровня, и полагается на базовый стек транспорта для фактического обмена данными с удаленной конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-104">Windows Sockets 2 incorporates the concept of a layered protocol: one that implements only higher-level communications functions while relying on an underlying transport stack for the actual exchange of data with a remote endpoint.</span></span> <span data-ttu-id="ad7e9-105">Примером такого типа многоуровневого протокола является уровень безопасности, который добавляет протокол к процессу подключения сокета для выполнения проверки подлинности и создания схемы шифрования.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-105">An example of this type of layered protocol is a security layer that adds a protocol to the socket connection process in order to perform authentication and establish an encryption scheme.</span></span> <span data-ttu-id="ad7e9-106">Для такого протокола безопасности обычно требуются службы базового и надежного транспортного протокола, такие как TCP или SPX.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-106">Such a security protocol generally requires the services of an underlying and reliable transport protocol such as TCP or SPX.</span></span>

<span data-ttu-id="ad7e9-107">Термин *базовый протокол* относится к протоколу, такому как TCP или SPX, который полностью способен выполнять обмен данными с удаленной конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-107">The term *base protocol* refers to a protocol, such as TCP or SPX, that is fully capable of performing data communications with a remote endpoint.</span></span> <span data-ttu-id="ad7e9-108">*Многоуровневый протокол* — это протокол, который не может быть изолирован, в то время как *цепочка протоколов* — один или несколько многоуровневых протоколов, набором связанных вместе и привязанные по базовому протоколу.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-108">A *layered protocol* is a protocol that cannot stand alone, while a *protocol chain* is one or more layered protocols strung together and anchored by a base protocol.</span></span>

<span data-ttu-id="ad7e9-109">Вы можете создать цепочку протоколов, если вы разрабатываете многоуровневые протоколы для поддержки SPI Windows Sockets 2 на обоих верхних и нижних краях.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-109">You can create a protocol chain if you design the layered protocols to support the Windows Sockets 2 SPI at both their upper and lower edges.</span></span> <span data-ttu-id="ad7e9-110">Особая [**Структура \_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) ссылается на цепочку протоколов в целом и описывает явный порядок, в котором объединены многоуровневые протоколы.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-110">A special [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure refers to the protocol chain as a whole and describes the explicit order in which the layered protocols are joined.</span></span> <span data-ttu-id="ad7e9-111">Это показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="ad7e9-111">This is illustrated in the figure below.</span></span> <span data-ttu-id="ad7e9-112">Поскольку приложения напрямую могут использовать только базовые протоколы и цепочки протоколов, они являются единственными из перечисленных, если установленные протоколы перечислены с помощью функции [**всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="ad7e9-112">Since only base protocols and protocol chains are directly usable by applications, they are the only ones listed when the installed protocols are enumerated with the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

![Архитектура многоуровневого протокола](images/ovrvw2-3.png)

 

 
