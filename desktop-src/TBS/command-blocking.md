---
title: Блокировка команд
description: Для сохранения целостности операций некоторые команды TPM не могут выполняться программным обеспечением на платформе.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104412744"
---
# <a name="command-blocking"></a><span data-ttu-id="5b53a-103">Блокировка команд</span><span class="sxs-lookup"><span data-stu-id="5b53a-103">Command Blocking</span></span>

<span data-ttu-id="5b53a-104">Для сохранения целостности операций некоторые команды TPM не могут выполняться программным обеспечением на платформе.</span><span class="sxs-lookup"><span data-stu-id="5b53a-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="5b53a-105">Например, некоторые команды выполняются только системным программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="5b53a-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="5b53a-106">Когда TBS блокирует команду, при необходимости возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="5b53a-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="5b53a-107">По умолчанию TBS блокирует команды, которые могут повлиять на конфиденциальность, безопасность и стабильность системы.</span><span class="sxs-lookup"><span data-stu-id="5b53a-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="5b53a-108">TBS также предполагает, что другие части программного стека могут ограничить доступ к определенным командам для полномочных сущностей.</span><span class="sxs-lookup"><span data-stu-id="5b53a-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="5b53a-109">Для команд TPM версии 1,2 существует три списка заблокированных команд: список, контролируемый групповой политикой, список, управляемый локальными администраторами, и список по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b53a-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="5b53a-110">Команда доверенного платформенного модуля блокируется, если она находится в любом из списков.</span><span class="sxs-lookup"><span data-stu-id="5b53a-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="5b53a-111">Однако существуют флаги групповой политики, позволяющие TBS игнорировать локальный список и список по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b53a-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="5b53a-112">Флаги групповой политики можно изменить напрямую или получить через редактор объектов групповой политики.</span><span class="sxs-lookup"><span data-stu-id="5b53a-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="5b53a-113">Список локально заблокированных команд не сохраняется после обновления операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5b53a-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="5b53a-114">Команды, заблокированные в списке групповая политика, сохраняются.</span><span class="sxs-lookup"><span data-stu-id="5b53a-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="5b53a-115">Для команд TPM версии 2,0 логика для блокировки инвертирована; в нем используется список разрешенных команд.</span><span class="sxs-lookup"><span data-stu-id="5b53a-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="5b53a-116">Эта логика автоматически блокирует команды, которые не были известны при первом внесении списка.</span><span class="sxs-lookup"><span data-stu-id="5b53a-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="5b53a-117">При добавлении команд в спецификацию TPM после доставки версии Windows эти новые команды автоматически блокируются.</span><span class="sxs-lookup"><span data-stu-id="5b53a-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="5b53a-118">Только обновление реестра добавит эти новые команды в список разрешенных команд.</span><span class="sxs-lookup"><span data-stu-id="5b53a-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="5b53a-119">Начиная с Windows 10 1809 (Windows Server 2019), разрешенные команды TPM 2,0 больше не могут управляться через параметры реестра.</span><span class="sxs-lookup"><span data-stu-id="5b53a-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="5b53a-120">В этих версиях Windows 10 разрешенные команды TPM 2,0 исправлены в драйвере TPM.</span><span class="sxs-lookup"><span data-stu-id="5b53a-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="5b53a-121">Команды TPM 1,2 по-прежнему могут блокироваться и разблокированы с помощью изменений в реестре.</span><span class="sxs-lookup"><span data-stu-id="5b53a-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="5b53a-122">Прямой доступ к реестру</span><span class="sxs-lookup"><span data-stu-id="5b53a-122">Direct Registry Access</span></span>

<span data-ttu-id="5b53a-123">Флаги групповая политика находятся в разделе реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Policies**( \\ **Microsoft** \\ **TPM** \\ **блоккедкоммандс**).</span><span class="sxs-lookup"><span data-stu-id="5b53a-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="5b53a-124">Чтобы определить, какие списки следует использовать для блокирования команд TPM, в качестве логических флагов используются два значения **типа DWORD** :</span><span class="sxs-lookup"><span data-stu-id="5b53a-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="5b53a-125">"Игноредефаултлист"</span><span class="sxs-lookup"><span data-stu-id="5b53a-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="5b53a-126">Если задано (значение существует и не равно нулю), то TBS игнорирует список заблокированных команд по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b53a-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="5b53a-127">"Игнорелокаллист"</span><span class="sxs-lookup"><span data-stu-id="5b53a-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="5b53a-128">Если задано (значение существует и не равно нулю), то TBS игнорирует список локальных заблокированных команд.</span><span class="sxs-lookup"><span data-stu-id="5b53a-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="5b53a-129">Редактор объектов групповой политики</span><span class="sxs-lookup"><span data-stu-id="5b53a-129">Group Policy Object Editor</span></span>

<span data-ttu-id="5b53a-130">**Доступ к редактору объектов групповая политика**</span><span class="sxs-lookup"><span data-stu-id="5b53a-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="5b53a-131">Щелкните **Запуск**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-131">Click **Start**.</span></span>
2.  <span data-ttu-id="5b53a-132">Нажмите кнопку **Запустить**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-132">Click **Run**.</span></span>
3.  <span data-ttu-id="5b53a-133">В окне **Открыть** введите **gpedit.msc**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="5b53a-134">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-134">Click **OK**.</span></span> <span data-ttu-id="5b53a-135">Откроется редактор объектов групповая политика.</span><span class="sxs-lookup"><span data-stu-id="5b53a-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="5b53a-136">Разверните узел **Конфигурация компьютера**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="5b53a-137">Разверните **Административные шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="5b53a-138">Разверните узел **система**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-138">Expand **System**.</span></span>
7.  <span data-ttu-id="5b53a-139">Разверните узел **доверенный платформенный модуль (TPM) службы**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="5b53a-140">Списки конкретных заблокированных команд TPM 1.2 можно изменять непосредственно в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="5b53a-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="5b53a-141">Список групповых политик:</span><span class="sxs-lookup"><span data-stu-id="5b53a-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="5b53a-142">Локальный список:</span><span class="sxs-lookup"><span data-stu-id="5b53a-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="5b53a-143">Список по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5b53a-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="5b53a-144">В каждом из этих разделов реестра имеется список значений реестра с \_ типом reg SZ.</span><span class="sxs-lookup"><span data-stu-id="5b53a-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="5b53a-145">Каждое значение представляет собой Заблокированную команду TPM.</span><span class="sxs-lookup"><span data-stu-id="5b53a-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="5b53a-146">Каждый раздел реестра содержит поле "имя значения" и поле "данные значения".</span><span class="sxs-lookup"><span data-stu-id="5b53a-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="5b53a-147">Оба поля ("имя значения" и "данные значения") должны точно соответствовать десятичному значению порядкового номера команды TPM, который будет заблокирован.</span><span class="sxs-lookup"><span data-stu-id="5b53a-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="5b53a-148">Список конкретных разрешенных команд TPM 2,0 можно изменить непосредственно в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="5b53a-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="5b53a-149">В разделе реестра содержится список значений реестра с \_ типом DWORD.</span><span class="sxs-lookup"><span data-stu-id="5b53a-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="5b53a-150">Каждое значение представляет разрешенную команду TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5b53a-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="5b53a-151">Каждое значение реестра имеет **имя** и поле **значения** .</span><span class="sxs-lookup"><span data-stu-id="5b53a-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="5b53a-152">**Имя** соответствует шестнадцатеричному порядковому номеру команды TPM 2,0, который должен быть разрешен.</span><span class="sxs-lookup"><span data-stu-id="5b53a-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="5b53a-153">**Значение** равно 1, если команда разрешена.</span><span class="sxs-lookup"><span data-stu-id="5b53a-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="5b53a-154">Если порядковый номер команды отсутствует или имеет значение 0, команда будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="5b53a-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="5b53a-155">Список по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="5b53a-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="5b53a-156">Для Windows 8, Windows Server 2012 и более поздних версий разделы реестра **блоккедкоммандс** и **AllowedW8Commands** , соответственно, определяют заблокированные или разрешенные команды TPM для учетных записей администратора.</span><span class="sxs-lookup"><span data-stu-id="5b53a-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="5b53a-157">Учетные записи пользователей имеют список заблокированных или разрешенных команд TPM в разделах реестра **блоккедусеркоммандс** и **AllowedW8UserCommands** соответственно.</span><span class="sxs-lookup"><span data-stu-id="5b53a-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="5b53a-158">В Windows 10 в версии 1607 появились новые разделы реестра для приложений AppContainer: **блоккедаппконтаинеркоммандс** и **AllowedW8AppContainerCommands**.</span><span class="sxs-lookup"><span data-stu-id="5b53a-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




