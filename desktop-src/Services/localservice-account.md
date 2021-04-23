---
description: Учетная запись LocalService представляет собой стандартную локальную учетную запись, используемую диспетчером управления службами.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Учетная запись LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546514"
---
# <a name="localservice-account"></a><span data-ttu-id="abccb-103">Учетная запись LocalService</span><span class="sxs-lookup"><span data-stu-id="abccb-103">LocalService Account</span></span>

<span data-ttu-id="abccb-104">Учетная запись LocalService представляет собой стандартную локальную учетную запись, используемую диспетчером управления службами.</span><span class="sxs-lookup"><span data-stu-id="abccb-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="abccb-105">Он имеет минимальные привилегии на локальном компьютере и представляет анонимные учетные данные в сети.</span><span class="sxs-lookup"><span data-stu-id="abccb-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="abccb-106">Эту учетную запись можно указать в вызове функций [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="abccb-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="abccb-107">Обратите внимание, что эта учетная запись не имеет пароля, поэтому любые сведения о пароле, предоставленные в этом вызове, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="abccb-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="abccb-108">Пока подсистема безопасности локализуется таким именем учетной записи, SCM не поддерживает локализованные имена.</span><span class="sxs-lookup"><span data-stu-id="abccb-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="abccb-109">Таким образом, вы получите локализованное имя для этой учетной записи из функции [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , но при вызове CreateService или чанжесервицеконфиг имя учетной записи должно быть локальной функцией NT Authority \\ LocalService, независимо от языкового стандарта, или могут возникнуть непредвиденные результаты.  </span><span class="sxs-lookup"><span data-stu-id="abccb-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="abccb-110">Идентификатор безопасности пользователя создается на основе значения **\_ RID локальной \_ службы \_ безопасности** .</span><span class="sxs-lookup"><span data-stu-id="abccb-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="abccb-111">Учетная запись LocalService имеет собственный подраздел в разделе реестра **hKey \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="abccb-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="abccb-112">Таким образом, раздел реестра **hKey \_ текущий \_ пользователь** связан с учетной записью LocalService.</span><span class="sxs-lookup"><span data-stu-id="abccb-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="abccb-113">Учетная запись LocalService имеет следующие права:</span><span class="sxs-lookup"><span data-stu-id="abccb-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="abccb-114">**SE \_ \_Имя ассигнпримаритокен** (отключено)</span><span class="sxs-lookup"><span data-stu-id="abccb-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="abccb-115">**SE \_ \_Имя аудита** (отключено)</span><span class="sxs-lookup"><span data-stu-id="abccb-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="abccb-116">**SE \_ ИЗМЕНИТЬ \_ \_ имя уведомления** (включено)</span><span class="sxs-lookup"><span data-stu-id="abccb-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="abccb-117">**SE \_ СОЗДАТЬ \_ глобальное \_ имя** (включено)</span><span class="sxs-lookup"><span data-stu-id="abccb-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="abccb-118">**SE \_ \_Имя олицетворения** (включено)</span><span class="sxs-lookup"><span data-stu-id="abccb-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="abccb-119">**SE \_ УВЕЛИЧИТЬ \_ \_ имя квоты** (отключено)</span><span class="sxs-lookup"><span data-stu-id="abccb-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="abccb-120">**SE \_ \_Имя завершения работы** (отключено)</span><span class="sxs-lookup"><span data-stu-id="abccb-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="abccb-121">**SE \_ Открепить \_ имя** (отключено)</span><span class="sxs-lookup"><span data-stu-id="abccb-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="abccb-122">Все привилегии, назначенные пользователям и прошедшим проверку пользователям</span><span class="sxs-lookup"><span data-stu-id="abccb-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="abccb-123">Дополнительные сведения см. в разделе [Безопасность службы и права доступа](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="abccb-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
