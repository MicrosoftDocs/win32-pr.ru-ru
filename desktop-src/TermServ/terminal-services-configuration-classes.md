---
title: Классы конфигурации службы удаленных рабочих столов
description: Поставщик WMI конфигурации службы удаленных рабочих столов предоставляет следующие классы. Иллюстрация приведена ниже.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413007"
---
# <a name="remote-desktop-services-configuration-classes"></a><span data-ttu-id="f5382-104">Классы конфигурации службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="f5382-104">Remote Desktop Services Configuration classes</span></span>

<span data-ttu-id="f5382-105">Поставщик WMI конфигурации службы удаленных рабочих столов предоставляет следующие классы.</span><span class="sxs-lookup"><span data-stu-id="f5382-105">The Remote Desktop Services Configuration WMI provider provides the following classes.</span></span> <span data-ttu-id="f5382-106">Иллюстрация приведена ниже.</span><span class="sxs-lookup"><span data-stu-id="f5382-106">An illustration follows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5382-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f5382-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f5382-108">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="f5382-108">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-109">Представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.</span><span class="sxs-lookup"><span data-stu-id="f5382-109">Represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-110">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f5382-110">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="f5382-111">Базовый класс для всех системных компонентов, представляющих абстрактные системные компоненты, такие как профили, процессы или возможности системы, в форме логических устройств.</span><span class="sxs-lookup"><span data-stu-id="f5382-111">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-112">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f5382-112">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="f5382-113">Базовый класс для иерархии системных элементов.</span><span class="sxs-lookup"><span data-stu-id="f5382-113">The base class for the system element hierarchy.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-114">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="f5382-114">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="f5382-115">Представляет связанные с конфигурацией и операционные параметры для одного или нескольких управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="f5382-115">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-116">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-116">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dd>

<span data-ttu-id="f5382-117">представляет терминал.</span><span class="sxs-lookup"><span data-stu-id="f5382-117">represents a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-118">**\_Терминалеррор Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-118">**Win32\_TerminalError**</span></span>](win32-terminalerror.md)
</dt> <dd>

<span data-ttu-id="f5382-119">Представляет ошибку терминала.</span><span class="sxs-lookup"><span data-stu-id="f5382-119">Represents a terminal error.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-120">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-120">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dd>

<span data-ttu-id="f5382-121">подкласс класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="f5382-121">a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="f5382-122">[**Win32 \_ Терминалсервице**](win32-terminalservice.md) представляет свойство **element** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f5382-122">[**Win32\_TerminalService**](win32-terminalservice.md) represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-123">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-123">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dd>

<span data-ttu-id="f5382-124">представляет конфигурацию для сервера узла сеансов удаленный рабочий стол сеансов (удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="f5382-124">represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-125">**\_Терминалсервицетосеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-125">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dd>

<span data-ttu-id="f5382-126">представляет связь между экземпляром класса [**Win32 \_ терминалсервице**](win32-terminalservice.md) и параметром определенного свойства [**\_ терминалсервицесеттинг Win32**](win32-terminalservicesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f5382-126">represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-127">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-127">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-128">представляет параметры, которые могут быть применены к терминалу.</span><span class="sxs-lookup"><span data-stu-id="f5382-128">represents the settings that can be applied to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-129">**\_Терминалтерминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-129">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-130">представляет связь между терминалом и его параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f5382-130">represents the association between a terminal and its configuration settings.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-131">**\_Тсаккаунт Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-131">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> <dd>

<span data-ttu-id="f5382-132">разрешает удаление учетной записи, которая существует на [**\_ терминале Win32**](win32-terminal.md) , и изменение существующих разрешений.</span><span class="sxs-lookup"><span data-stu-id="f5382-132">allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-133">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-133">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-134">Определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , связанного с политикой подключения.</span><span class="sxs-lookup"><span data-stu-id="f5382-134">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-135">**\_Тсдисковередлиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-135">**Win32\_TSDiscoveredLicenseServer**</span></span>](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

<span data-ttu-id="f5382-136">Предоставляет сведения об обнаруженном сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="f5382-136">Provides details about the discovered Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-137">**\_Тсенвиронментсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-138">Определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , включая политику начальной программы.</span><span class="sxs-lookup"><span data-stu-id="f5382-138">defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-139">**\_Тсженералсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-139">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-140">представляет общие параметры терминала, такие как уровень шифрования и транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="f5382-140">represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-141">**\_Тслогонсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-142">Определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , связанного с входом клиента.</span><span class="sxs-lookup"><span data-stu-id="f5382-142">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-143">**\_Тснетворкадаптерлистсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-143">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-144">Перечисляет список сетевых адаптеров, которые могут быть настроены для [**\_ терминала Win32**](win32-terminal.md)на основе указанного протокола и метода транспорта.</span><span class="sxs-lookup"><span data-stu-id="f5382-144">enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-145">**\_Тснетворкадаптерсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-145">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> <dd>

<span data-ttu-id="f5382-146">Определяет различные параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , включая свойства, связанные с сетевым адаптером, и максимальное разрешенное число подключений.</span><span class="sxs-lookup"><span data-stu-id="f5382-146">defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-147">**\_Тспермиссионссеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-147">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> <dd>

<span data-ttu-id="f5382-148">включает метод для добавления новых учетных записей в терминал и метод восстановления разрешений по умолчанию для терминала.</span><span class="sxs-lookup"><span data-stu-id="f5382-148">includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-149">**\_Тсремотеконтролсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-150">Определяет параметры конфигурации удаленного управления для класса [**\_ терминала Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="f5382-150">defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-151">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-151">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dd>

<span data-ttu-id="f5382-152">Определяет параметры конфигурации подключение к удаленному рабочему столу Broker (RDCB) для класса [**Win32 \_ тссессиондиректорисеттинг**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f5382-152">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-153">**\_Тссессиондиректорисеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-153">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> <dd>

<span data-ttu-id="f5382-154">Представляет связь между экземпляром класса [**Win32 \_ терминалсервице**](win32-terminalservice.md) и экземпляром класса [**\_ тссессиондиректори Win32**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="f5382-154">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-155">**\_Тссессионсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-155">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-156">Определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , такие как ограничения времени, а также действия по отсоединению и повторному подключению.</span><span class="sxs-lookup"><span data-stu-id="f5382-156">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-157">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-157">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> <dd>

<span data-ttu-id="f5382-158">Определяет параметры виртуализации IP для сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f5382-158">Defines Internet protocol (IP) virtualization settings for a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="f5382-159">**\_Тсвиртуалипсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f5382-159">**Win32\_TSVirtualIPSetting**</span></span>](win32-tsvirtualipsetting.md)
</dt> <dd>

<span data-ttu-id="f5382-160">Представляет ассоциацию между классом элемента [**Win32 \_ терминалсервице**](win32-terminalservice.md) и классом параметра [**Win32 \_ тсвиртуалип**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="f5382-160">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

</dd> </dl>

<span data-ttu-id="f5382-161">На следующем рисунке показаны связи между этими классами.</span><span class="sxs-lookup"><span data-stu-id="f5382-161">The following illustration shows the relationships between these classes.</span></span>

![связи между поддерживаемыми классами](images/tswmi.png)

 

 