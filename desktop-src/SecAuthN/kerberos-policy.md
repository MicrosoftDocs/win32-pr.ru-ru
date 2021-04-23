---
description: Политика билета Kerberos определяется на уровне домена и реализуется центр распространения ключейом домена (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Политика Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650840"
---
# <a name="kerberos-policy"></a><span data-ttu-id="6a5e7-103">Политика Kerberos</span><span class="sxs-lookup"><span data-stu-id="6a5e7-103">Kerberos Policy</span></span>

<span data-ttu-id="6a5e7-104">Политика билета Kerberos определяется на уровне домена и реализуется [*центр распространения ключейом*](../secgloss/k-gly.md) домена (KDC).</span><span class="sxs-lookup"><span data-stu-id="6a5e7-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="6a5e7-105">Политика Kerberos хранится в Active Directory в качестве подмножества атрибутов политики безопасности домена.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="6a5e7-106">По умолчанию параметры политики могут быть заданы только членами группы "Администраторы домена".</span><span class="sxs-lookup"><span data-stu-id="6a5e7-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="6a5e7-107">Политика домена включает следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="6a5e7-108">Поддержка билетов, датированных будущим числом</span><span class="sxs-lookup"><span data-stu-id="6a5e7-108">Support postdated tickets</span></span>
-   <span data-ttu-id="6a5e7-109">Поддержка ограниченного делегирования (только Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="6a5e7-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="6a5e7-110">Запросы в службу поддержки, которые можно перенаправить</span><span class="sxs-lookup"><span data-stu-id="6a5e7-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="6a5e7-111">Поддержка билетов устанавливать возобновляемую</span><span class="sxs-lookup"><span data-stu-id="6a5e7-111">Support renewable tickets</span></span>
-   <span data-ttu-id="6a5e7-112">Задать максимальный возраст билета</span><span class="sxs-lookup"><span data-stu-id="6a5e7-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="6a5e7-113">Задать максимальный возраст продления</span><span class="sxs-lookup"><span data-stu-id="6a5e7-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="6a5e7-114">Задать максимальный срок действия билета прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="6a5e7-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="6a5e7-115">Принудительное завершение работы пользователей при истечении срока действия билетов</span><span class="sxs-lookup"><span data-stu-id="6a5e7-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="6a5e7-116">При [*ограниченном делегировании*](../secgloss/c-gly.md)компьютер может быть настроен на разрешение пересылки учетных данных только в конкретный список служб.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="6a5e7-117">Эти службы должны находиться в том же домене, что и компьютер, пересылая учетные данные.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="6a5e7-118">При *ограниченном делегировании* билеты больше не отправляются с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="6a5e7-119">Серверный компьютер создает билеты службы для пересылки по мере необходимости из сведений, используемых для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="6a5e7-120">Хотя политика Kerberos для домена может разрешить делегированную проверку подлинности, разрешая переадресацию билетов, этот аспект политики не должен применяться ко всем пользователям или компьютерам.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="6a5e7-121">Атрибут учетной записи отдельного пользователя можно настроить для отключения перенаправления [*учетных данных*](../secgloss/c-gly.md) этого пользователя любым сервером.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="6a5e7-122">Атрибут учетной записи отдельного компьютера можно настроить для отключения пересылки учетных данных от любого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="6a5e7-123">В обоих случаях делегирование можно отключить, создав групповую политику, которая будет применяться ко всем пользователям или всем компьютерам в подразделении Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="6a5e7-124">**Windows XP и 2000:** Ограниченное делегирование не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6a5e7-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 
