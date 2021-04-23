---
description: Объясняет взаимодействие между службами Winlogon и Network Provider.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Взаимодействие с поставщиками сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912475"
---
# <a name="interaction-with-network-providers"></a><span data-ttu-id="8445c-103">Взаимодействие с поставщиками сети</span><span class="sxs-lookup"><span data-stu-id="8445c-103">Interaction with Network Providers</span></span>

<span data-ttu-id="8445c-104">Можно настроить систему для поддержки одного или нескольких поставщиков сети.</span><span class="sxs-lookup"><span data-stu-id="8445c-104">You can configure a system to support zero or more network providers.</span></span> <span data-ttu-id="8445c-105">Каждый из этих поставщиков сети может указать, что для него требуется специальная интерактивная обработка проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8445c-105">Each of these network providers can specify that it requires special interactive authentication processing.</span></span> <span data-ttu-id="8445c-106">Эта возможность позволяет установленным сетям получать сведения о идентификации и проверке подлинности, относящиеся к каждой сети, но позволяет им сохранять их во время обычного входа в систему, а также в защищенный тег [*контекста*](../secgloss/c-gly.md) и рабочего стола [*Winlogon*](../secgloss/w-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8445c-106">This capability allows installed networks to collect identification and authentication information specific to each network, yet allows them to collect it during normal logon and under the secure umbrella of [*Winlogon's*](../secgloss/w-gly.md) [*context*](../secgloss/c-gly.md) and desktop.</span></span>

<span data-ttu-id="8445c-107">Winlogon вызывает сетевые поставщики в ряде случаев.</span><span class="sxs-lookup"><span data-stu-id="8445c-107">Winlogon calls network providers under a number of circumstances.</span></span> <span data-ttu-id="8445c-108">После успешного входа в систему Winlogon вызывает поставщиков сети, чтобы они могли получать [*учетные данные*](../secgloss/c-gly.md) и проверять подлинность пользователя в сети.</span><span class="sxs-lookup"><span data-stu-id="8445c-108">Following a successful logon, Winlogon calls network providers so they can collect [*credentials*](../secgloss/c-gly.md) and authenticate the user for their network.</span></span> <span data-ttu-id="8445c-109">Winlogon также вызывает поставщиков сети, когда пользователи меняют свои пароли.</span><span class="sxs-lookup"><span data-stu-id="8445c-109">Winlogon also calls network providers when users change their passwords.</span></span> <span data-ttu-id="8445c-110">Это позволяет каждому пользователю поддерживать один пароль для использования во всех сетях.</span><span class="sxs-lookup"><span data-stu-id="8445c-110">This lets each user maintain a single password for use on all networks.</span></span>

<span data-ttu-id="8445c-111">Структура [**\_ \_ \_ сведений об уведомлении влкс MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) используется для предоставления сведений об идентификации и проверке подлинности в соответствующих функциях GINA.</span><span class="sxs-lookup"><span data-stu-id="8445c-111">The [**WLX\_MPR\_NOTIFY\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) structure is used to provide identification and authentication information in the relevant GINA functions.</span></span> <span data-ttu-id="8445c-112">Эта структура включает следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="8445c-112">This structure includes the following members.</span></span>



| <span data-ttu-id="8445c-113">Член</span><span class="sxs-lookup"><span data-stu-id="8445c-113">Member</span></span>             | <span data-ttu-id="8445c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8445c-114">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8445c-115">**псзусернаме**</span><span class="sxs-lookup"><span data-stu-id="8445c-115">**pszUserName**</span></span>    | <span data-ttu-id="8445c-116">Имя учетной записи пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="8445c-116">The account name of the logged-on user.</span></span>                                                                                                                                                      |
| <span data-ttu-id="8445c-117">**псздомаин**</span><span class="sxs-lookup"><span data-stu-id="8445c-117">**pszDomain**</span></span>      | <span data-ttu-id="8445c-118">Доменное имя вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="8445c-118">The domain name of the logged-on user.</span></span> <span data-ttu-id="8445c-119">Не все модели проверки подлинности имеют понятие предметной области (или его эквивалент), поэтому этот член может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8445c-119">Not all authentication models have a domain concept (or its equivalent), so this member can be **NULL**.</span></span>                                              |
| <span data-ttu-id="8445c-120">**псзпассворд**</span><span class="sxs-lookup"><span data-stu-id="8445c-120">**pszPassword**</span></span>    | <span data-ttu-id="8445c-121">Когда пользователь выдает пароль в виде открытого текста во время проверки подлинности, его предоставление здесь позволяет другим поставщикам сети использовать один и тот же пароль (для обеспечения единого входа) без запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="8445c-121">When the user gave a plaintext password during authentication, providing it here lets other network providers use the same password (to achieve single logon) without prompting the user.</span></span>    |
| <span data-ttu-id="8445c-122">**псзолдпассворд**</span><span class="sxs-lookup"><span data-stu-id="8445c-122">**pszOldPassword**</span></span> | <span data-ttu-id="8445c-123">После изменения пароля, указав исходный пароль и новый пароль в члене **псзпассворд** , поставщики сетевых услуг обновляют свои пароли без запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="8445c-123">After a password change, providing the original password here and the new password in the **pszPassword** member, lets network providers upgrade their passwords without prompting the user.</span></span> |



 

<span data-ttu-id="8445c-124">[*GINA*](../secgloss/g-gly.md) не требуется предоставлять эту информацию поставщикам сети.</span><span class="sxs-lookup"><span data-stu-id="8445c-124">A [*GINA*](../secgloss/g-gly.md) does not have to provide this information to network providers.</span></span> <span data-ttu-id="8445c-125">Если вместо указателя на структуру передается указатель **null** , поставщики сети будут запрашивать у пользователя сведения.</span><span class="sxs-lookup"><span data-stu-id="8445c-125">If a **NULL** pointer is passed instead of a valid structure pointer, the network providers will prompt the user for information.</span></span>

 

 
