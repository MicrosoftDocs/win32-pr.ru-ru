---
description: — Это модуль Windows, который выполняет интерактивный вход в сеанс входа в систему. Поведение Winlogon можно настроить путем реализации и регистрации поставщика учетных данных.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon и поставщики учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991056"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="9516f-104">Winlogon и поставщики учетных данных</span><span class="sxs-lookup"><span data-stu-id="9516f-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="9516f-105">[*Winlogon*](../secgloss/w-gly.md) — это модуль Windows, который выполняет интерактивный вход в [*сеанс входа*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9516f-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="9516f-106">Поведение Winlogon можно настроить путем реализации и регистрации поставщика учетных данных.</span><span class="sxs-lookup"><span data-stu-id="9516f-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="9516f-107">Сведения о реализации поставщика учетных данных см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="9516f-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="9516f-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="9516f-108">Topic</span></span>                                                                                                           | <span data-ttu-id="9516f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9516f-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9516f-110">Интерфейс входа Windows, управляемый поставщиком учетных данных</span><span class="sxs-lookup"><span data-stu-id="9516f-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="9516f-111">Общие сведения об архитектуре Winlogon и поставщика учетных данных и пример поставщика учетных данных.</span><span class="sxs-lookup"><span data-stu-id="9516f-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="9516f-112">Интерфейсы оболочки</span><span class="sxs-lookup"><span data-stu-id="9516f-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="9516f-113">Справочник по интерфейсу поставщика учетных данных.</span><span class="sxs-lookup"><span data-stu-id="9516f-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="9516f-114">Поставщики учетных данных в Windows 10</span><span class="sxs-lookup"><span data-stu-id="9516f-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="9516f-115">Сторонние поставщики учетных данных и системные поставщики учетных данных в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9516f-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="9516f-116">Пример реализации поставщика учетных данных см. в примере, расположенном в каталоге установки Windows SDK в разделе \\ Samples \\ Security \\ кредентиалпровидер.</span><span class="sxs-lookup"><span data-stu-id="9516f-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="9516f-117">**Windows Server 2003 и Windows XP:** Поставщики учетных данных не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9516f-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="9516f-118">Сведения о настройке Winlogon см. в разделе [Winlogon и GINA](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="9516f-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
