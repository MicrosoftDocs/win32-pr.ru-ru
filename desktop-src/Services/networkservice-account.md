---
description: Учетная запись NetworkService представляет собой стандартную локальную учетную запись, используемую диспетчером управления службами.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Учетная запись NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664199"
---
# <a name="networkservice-account"></a><span data-ttu-id="d9560-103">Учетная запись NetworkService</span><span class="sxs-lookup"><span data-stu-id="d9560-103">NetworkService Account</span></span>

<span data-ttu-id="d9560-104">Учетная запись NetworkService представляет собой стандартную локальную учетную запись, используемую диспетчером управления службами.</span><span class="sxs-lookup"><span data-stu-id="d9560-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="d9560-105">Эта учетная запись не распознается подсистемой безопасности, поэтому нельзя указать ее имя в вызове функции [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .</span><span class="sxs-lookup"><span data-stu-id="d9560-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="d9560-106">Он имеет минимальные права на локальном компьютере и действует как компьютер в сети.</span><span class="sxs-lookup"><span data-stu-id="d9560-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="d9560-107">Эту учетную запись можно указать в вызове функций [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="d9560-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="d9560-108">Обратите внимание, что эта учетная запись не имеет пароля, поэтому любые сведения о пароле, предоставленные в этом вызове, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="d9560-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="d9560-109">Пока подсистема безопасности локализуется таким именем учетной записи, SCM не поддерживает локализованные имена.</span><span class="sxs-lookup"><span data-stu-id="d9560-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="d9560-110">Поэтому вы получите локализованное имя для этой учетной записи из функции [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , но при вызове CreateService или чанжесервицеконфиг имя учетной записи должно быть "NT Authority \\ NetworkService ", независимо от языкового стандарта или непредвиденных результатов. </span><span class="sxs-lookup"><span data-stu-id="d9560-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="d9560-111">Служба, которая выполняется в контексте учетной записи NetworkService, представляет учетные данные компьютера удаленным серверам.</span><span class="sxs-lookup"><span data-stu-id="d9560-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="d9560-112">По умолчанию удаленный токен содержит идентификаторы безопасности для групп «все» и «пользователи, прошедшие проверку».</span><span class="sxs-lookup"><span data-stu-id="d9560-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="d9560-113">Идентификатор безопасности пользователя создается на основе значения **\_ RID сетевой \_ службы \_ безопасности** .</span><span class="sxs-lookup"><span data-stu-id="d9560-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="d9560-114">Учетная запись NetworkService имеет собственный подраздел в разделе реестра **hKey \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="d9560-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="d9560-115">Таким образом, раздел реестра **hKey \_ текущий \_ пользователь** связан с учетной записью NetworkService.</span><span class="sxs-lookup"><span data-stu-id="d9560-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="d9560-116">Учетная запись NetworkService имеет следующие права:</span><span class="sxs-lookup"><span data-stu-id="d9560-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="d9560-117">**SE \_ \_Имя ассигнпримаритокен** (отключено)</span><span class="sxs-lookup"><span data-stu-id="d9560-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="d9560-118">**SE \_ \_Имя аудита** (отключено)</span><span class="sxs-lookup"><span data-stu-id="d9560-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="d9560-119">**SE \_ ИЗМЕНИТЬ \_ \_ имя уведомления** (включено)</span><span class="sxs-lookup"><span data-stu-id="d9560-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="d9560-120">**SE \_ СОЗДАТЬ \_ глобальное \_ имя** (включено)</span><span class="sxs-lookup"><span data-stu-id="d9560-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="d9560-121">**SE \_ \_Имя олицетворения** (включено)</span><span class="sxs-lookup"><span data-stu-id="d9560-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="d9560-122">**SE \_ УВЕЛИЧИТЬ \_ \_ имя квоты** (отключено)</span><span class="sxs-lookup"><span data-stu-id="d9560-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="d9560-123">**SE \_ \_Имя завершения работы** (отключено)</span><span class="sxs-lookup"><span data-stu-id="d9560-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="d9560-124">**SE \_ Открепить \_ имя** (отключено)</span><span class="sxs-lookup"><span data-stu-id="d9560-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="d9560-125">Все привилегии, назначенные пользователям и прошедшим проверку пользователям</span><span class="sxs-lookup"><span data-stu-id="d9560-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="d9560-126">Дополнительные сведения см. в разделе [Безопасность службы и права доступа](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="d9560-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
