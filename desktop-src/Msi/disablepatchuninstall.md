---
description: Если для этой системной политики на уровне компьютера установлено значение 1, исправления не могут быть удалены с компьютера пользователем или администратором.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: дисаблепатчунинсталл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897810"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="5285b-103">дисаблепатчунинсталл</span><span class="sxs-lookup"><span data-stu-id="5285b-103">DisablePatchUninstall</span></span>

<span data-ttu-id="5285b-104">Если для этой [системной политики](system-policy.md) на уровне компьютера установлено значение 1, исправления не могут быть удалены с компьютера пользователем или администратором.</span><span class="sxs-lookup"><span data-stu-id="5285b-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="5285b-105">Установщик Windows может по-прежнему удалить исправление, которое больше не применимо к продукту.</span><span class="sxs-lookup"><span data-stu-id="5285b-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="5285b-106">Если эта политика не задана, пользователь может удалить исправление с компьютера, только если ему предоставлены права на удаление исправления.</span><span class="sxs-lookup"><span data-stu-id="5285b-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="5285b-107">Это может зависеть от того, является ли пользователь администратором, установлены ли параметры политики [дисаблемси](disablemsi.md) и [AlwaysInstallElevated](alwaysinstallelevated.md) и установлено ли это исправление в управляемом пользователем, неуправляемом или отдельном для пользователя контексте.</span><span class="sxs-lookup"><span data-stu-id="5285b-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="5285b-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="5285b-108">Registry Key</span></span>

<span data-ttu-id="5285b-109">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="5285b-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="5285b-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5285b-110">Data Type</span></span>

<span data-ttu-id="5285b-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5285b-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="5285b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="5285b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5285b-113">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="5285b-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



