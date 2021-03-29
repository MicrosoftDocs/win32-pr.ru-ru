---
title: О NAP
description: О NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773361"
---
# <a name="about-nap"></a><span data-ttu-id="76d9c-103">О NAP</span><span class="sxs-lookup"><span data-stu-id="76d9c-103">About NAP</span></span>

> [!Note]  
> <span data-ttu-id="76d9c-104">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="76d9c-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="76d9c-105">Защита доступа к сети (NAP) предназначена для того, чтобы помочь администраторам в обслуживании работоспособности компьютеров в сети, что в своюмся образом помогает поддерживать общую целостность сети.</span><span class="sxs-lookup"><span data-stu-id="76d9c-105">Network Access Protection (NAP) is designed to help administrators maintain the health of the computers on the network, which in turns helps maintain the overall integrity of the network.</span></span> <span data-ttu-id="76d9c-106">Он не предназначен для защиты сети от злонамеренных пользователей.</span><span class="sxs-lookup"><span data-stu-id="76d9c-106">It is not designed to secure a network from malicious users.</span></span> <span data-ttu-id="76d9c-107">Например, если на компьютере установлено все программное обеспечение и конфигурации, необходимые политике сетевого доступа, компьютер считается работоспособным или соответствующим требованиям, и ему будет предоставлен соответствующий доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="76d9c-107">For example, if a computer has all the software and configurations that the network access policy requires, the computer is considered healthy or compliant, and it will be granted the appropriate access to the network.</span></span> <span data-ttu-id="76d9c-108">Защита доступа к сети не запрещает полномочным пользователям, соответствующим компьютеру, загружать вредоносную программу в сеть или влиять на другое неприемлемое поведение.</span><span class="sxs-lookup"><span data-stu-id="76d9c-108">NAP does not prevent an authorized user with a compliant computer from uploading a malicious program to the network or engaging in other inappropriate behavior.</span></span>

<span data-ttu-id="76d9c-109">Для защиты доступа к сети сетевая инфраструктура должна предоставить следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="76d9c-109">To protect access to a network, a network infrastructure needs to provide the following areas of functionality:</span></span>

-   <span data-ttu-id="76d9c-110">Проверка работоспособности: определяет, соответствуют ли компьютеры требованиям к работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="76d9c-110">Health validation: Determines whether the computers are compliant with system health requirements.</span></span>
-   <span data-ttu-id="76d9c-111">Ограничение сети: ограничение доступа к сети или связи для клиентов, которые не соответствуют требованиям к работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="76d9c-111">Network restriction: Restricts access to the network or communication for clients that do not comply with system health requirements.</span></span>
-   <span data-ttu-id="76d9c-112">Исправление: предоставляет необходимые обновления, чтобы разрешить компьютеру исправить несоответствующее состояние работоспособности.</span><span class="sxs-lookup"><span data-stu-id="76d9c-112">Remediation: Provides necessary updates to allow the computer to correct its noncompliant health state.</span></span>
-   <span data-ttu-id="76d9c-113">Текущее соответствие: разрешает доступ к сети при условии, что компьютер пользователя соответствует требованиям политики работоспособности.</span><span class="sxs-lookup"><span data-stu-id="76d9c-113">Ongoing compliance: Permits access to the network as long as the user's computer meets health policy requirements.</span></span>

<span data-ttu-id="76d9c-114">Windows XP с пакетом обновления 3 (SP3), Windows Vista и Windows Server 2008 предоставляют методы принудительного применения защиты доступа к сети для конфигурации DHCP-адресов, подключений виртуальной частной сети на основе удаленного доступа (VPN), проводных и беспроводных подключений IEEE 802.1 X, прошедших проверку подлинности и беспроводной связи на основе протокола IPsec.</span><span class="sxs-lookup"><span data-stu-id="76d9c-114">Windows XP with Service Pack 3 (SP3), Windows Vista, and Windows Server 2008 provide NAP enforcement methods for Dynamic Host Configuration Protocol (DHCP) address configuration, remote access-based virtual private network (VPN) connections, IEEE 802.1X-authenticated wired and wireless connections, and Internet Protocol security (IPsec)-based communications.</span></span> <span data-ttu-id="76d9c-115">Платформа NAP также поддерживает архитектуру, с помощью которой можно выполнять проверку работоспособности, ограничение сети, исправление и текущее соответствие требованиям для дополнительных компонентов, которые могут предоставляться сторонними поставщиками программного обеспечения или корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="76d9c-115">The NAP platform additionally supports an architecture through which health validation, network restriction, remediation, and ongoing compliance are supported by additional components that can be supplied by third-party software vendors or by Microsoft.</span></span>

<span data-ttu-id="76d9c-116">Платформа NAP включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="76d9c-116">The NAP platform includes the following components:</span></span>

-   [<span data-ttu-id="76d9c-117">Архитектура клиента NAP</span><span class="sxs-lookup"><span data-stu-id="76d9c-117">NAP Client Architecture</span></span>](nap-client-architecture.md)
-   [<span data-ttu-id="76d9c-118">Архитектура защиты доступа к сети на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="76d9c-118">NAP Server-side Architecture</span></span>](nap-server-side-architecture.md)
-   [<span data-ttu-id="76d9c-119">Взаимодействие клиента NAP и компонентов на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="76d9c-119">NAP Client and Server-side Component Communication</span></span>](nap-client-and-server-side-component-communication.md)

<span data-ttu-id="76d9c-120">Для клиента NAP требуется Windows Vista, Windows XP с пакетом обновления 3 (SP3) или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="76d9c-120">The NAP client requires Windows Vista, Windows XP with SP3, or Windows Server 2008.</span></span> <span data-ttu-id="76d9c-121">Для сервера политики работоспособности NAP и точек принудительного применения NAP для использования DHCP, VPN и IPsec требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="76d9c-121">The NAP health policy server and NAP enforcement points for DHCP, VPN, and IPsec enforcement require Windows Server 2008.</span></span>

 

 




