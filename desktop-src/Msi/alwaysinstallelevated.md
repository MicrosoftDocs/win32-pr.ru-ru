---
description: Установите пакет установщик Windows с повышенными правами (System).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545194"
---
# <a name="alwaysinstallelevated"></a><span data-ttu-id="11027-103">AlwaysInstallElevated</span><span class="sxs-lookup"><span data-stu-id="11027-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="11027-104">Вы можете использовать политику AlwaysInstallElevated для установки пакета установщик Windows с повышенными правами (System).</span><span class="sxs-lookup"><span data-stu-id="11027-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="11027-105">\* \* Предупреждение: \* \*</span><span class="sxs-lookup"><span data-stu-id="11027-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="11027-106">Этот параметр аналогичен предоставлению полных прав администратора, что может представлять значительный риск безопасности.</span><span class="sxs-lookup"><span data-stu-id="11027-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="11027-107">Корпорация Майкрософт настоятельно не рекомендует использовать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="11027-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="11027-108">Чтобы установить пакет с повышенными правами (системным), задайте для параметра AlwaysInstallElevated значение 1 в обоих следующих разделах реестра:</span><span class="sxs-lookup"><span data-stu-id="11027-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="11027-109">**HKey \_ Текущие \_ политики пользовательского** \\ **программного обеспечения** \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="11027-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="11027-110">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="11027-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="11027-111">Если значение AlwaysInstallElevated не равно 1 в обоих указанных выше разделах реестра, установщик использует повышенные привилегии для установки управляемых приложений и использует уровень привилегий текущего пользователя для неуправляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="11027-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="11027-112">Так как эта политика позволяет пользователям устанавливать приложения, которым требуется доступ к каталогам и разделам реестра, для которых пользователь может не иметь разрешения на просмотр или изменение, следует подумать, предоставляет ли пользователи соответствующий уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="11027-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="11027-113">Установка этой политики направляет установщик Windows использовать системные разрешения при установке приложения в системе.</span><span class="sxs-lookup"><span data-stu-id="11027-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="11027-114">Если эта политика не задана, приложения, не распространяемые администратором, устанавливаются с использованием привилегий пользователя, и только управляемые приложения получают повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="11027-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="11027-115">Обратите внимание, что после включения политики для каждого компьютера для AlwaysInstallElevated любой пользователь может задать параметры для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="11027-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="11027-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11027-116">Remarks</span></span>

<span data-ttu-id="11027-117">Сведения о взаимодействии этой политики с источниками установки см. в разделе [Управление источниками установки](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="11027-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="11027-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="11027-118">Data Type</span></span>

<span data-ttu-id="11027-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="11027-119">**REG\_DWORD**</span></span>

 

 



