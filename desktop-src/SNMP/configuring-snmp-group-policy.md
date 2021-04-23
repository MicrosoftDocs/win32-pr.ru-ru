---
title: Настройка SNMP-групповая политика
description: При использовании оснастки консоли управления (MMC) для групповая политика администрирования параметров политики на основе реестра, применяемых к SNMP, могут существовать один или несколько следующих подразделов.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134347"
---
# <a name="configuring-snmp-group-policy"></a><span data-ttu-id="46020-103">Настройка SNMP-групповая политика</span><span class="sxs-lookup"><span data-stu-id="46020-103">Configuring SNMP Group Policy</span></span>

<span data-ttu-id="46020-104">При использовании оснастки консоли управления (MMC) для групповая политика администрирования параметров политики на основе реестра, применяемых к SNMP, могут существовать один или несколько следующих подразделов.</span><span class="sxs-lookup"><span data-stu-id="46020-104">If you use the Microsoft Management Console (MMC) snap-in for Group Policy to administer registry-based policy settings that apply to SNMP, one or more of the following subkeys may exist.</span></span>

<span data-ttu-id="46020-105">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера — \\  \\  \\ **Параметры** SNMP \\ **валидкоммунитиес**</span><span class="sxs-lookup"><span data-stu-id="46020-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="46020-106">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера — \\  \\  \\ **Параметры** SNMP \\ **пермиттедманажерс**</span><span class="sxs-lookup"><span data-stu-id="46020-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="46020-107">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера — \\  \\  \\ **Параметры** SNMP \\ **трапконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="46020-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**TrapConfiguration**</span></span>

<span data-ttu-id="46020-108">Как правило, только члены локальной группы "Администраторы" могут получить доступ к следующим подразделам реестра, в которых хранятся данные конфигурации для службы SNMP:</span><span class="sxs-lookup"><span data-stu-id="46020-108">Typically, only members of the Administrators local group can access the following registry subkeys that store configuration data for the SNMP service:</span></span>

<span data-ttu-id="46020-109">**HKey \_ \_** \\  \\  \\  \\ **Параметры протокола SNMP** \\ для CurrentControlSet Services \\  системы локального компьютера валидкоммунитиес</span><span class="sxs-lookup"><span data-stu-id="46020-109">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="46020-110">**HKey \_ \_** \\  \\  \\  \\ **Параметры протокола SNMP** \\ для CurrentControlSet Services \\  системы локального компьютера пермиттедманажерс</span><span class="sxs-lookup"><span data-stu-id="46020-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="46020-111">Дополнительные сведения о параметрах политики на основе реестра см. в разделе [about групповая политика](/previous-versions/windows/desktop/Policy/about-group-policy).</span><span class="sxs-lookup"><span data-stu-id="46020-111">For more information about registry-based policy settings, see [About Group Policy](/previous-versions/windows/desktop/Policy/about-group-policy).</span></span>

 

 