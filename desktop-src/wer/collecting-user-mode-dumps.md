---
title: Сбор дампов User-Mode
description: Начиная с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1) отчеты об ошибках Windows (WER) можно настроить таким образом, чтобы полные дампы пользовательского режима собираются и сохранялись локально после сбоя приложения пользовательского режима.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890459"
---
# <a name="collecting-user-mode-dumps"></a><span data-ttu-id="9c8bd-103">Сбор дампов User-Mode</span><span class="sxs-lookup"><span data-stu-id="9c8bd-103">Collecting User-Mode Dumps</span></span>

<span data-ttu-id="9c8bd-104">Начиная с Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1) отчеты об ошибках Windows (WER) можно настроить таким образом, чтобы полные дампы пользовательского режима собираются и сохранялись локально после сбоя приложения пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-104">Starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1), Windows Error Reporting (WER) can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes.</span></span> <span data-ttu-id="9c8bd-105">Приложения, которые выполняют пользовательские отчеты о сбоях, включая приложения .NET, не поддерживаются этой функцией.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-105">Applications that do their own custom crash reporting, including .NET applications, are not supported by this feature.</span></span>

<span data-ttu-id="9c8bd-106">Эта функция отключена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-106">This feature is not enabled by default.</span></span> <span data-ttu-id="9c8bd-107">Для включения функции требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-107">Enabling the feature requires administrator privileges.</span></span> <span data-ttu-id="9c8bd-108">Чтобы включить и настроить функцию, используйте следующие значения реестра в разделе **\_ \_ программное обеспечение для локального компьютера HKEY \\ \\ Microsoft \\ Windows \\ отчеты об ошибках Windows \\ локалдумпс** Key.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-108">To enable and configure the feature, use the following registry values under the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** key.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c8bd-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9c8bd-109">Value</span></span></th>
<th><span data-ttu-id="9c8bd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9c8bd-110">Description</span></span></th>
<th><span data-ttu-id="9c8bd-111">Тип</span><span class="sxs-lookup"><span data-stu-id="9c8bd-111">Type</span></span></th>
<th><span data-ttu-id="9c8bd-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9c8bd-112">Default value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c8bd-113"><strong>думпфолдер</strong></span><span class="sxs-lookup"><span data-stu-id="9c8bd-113"><strong>DumpFolder</strong></span></span></td>
<td><span data-ttu-id="9c8bd-114">Путь, по которому должны храниться файлы дампа.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-114">The path where the dump files are to be stored.</span></span> <span data-ttu-id="9c8bd-115">Если путь по умолчанию не используется, убедитесь, что в папке содержатся списки управления доступом, позволяющие процессу аварийного завершения записывать данные в папку.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-115">If you do not use the default path, then make sure that the folder contains ACLs that allow the crashing process to write data to the folder.</span></span> <span data-ttu-id="9c8bd-116">Для сбоев службы дамп записывается в папки профиля конкретной службы в зависимости от используемой учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-116">For service crashes, the dump is written to service specific profile folders depending on the service account used.</span></span> <span data-ttu-id="9c8bd-117">Например, папка Profile для системных служб —%WINDIR%\System32\Config\SystemProfile.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-117">For example, the profile folder for System services is %WINDIR%\System32\Config\SystemProfile.</span></span> <span data-ttu-id="9c8bd-118">Для сетевых и локальных служб папка является%Виндир%\сервицепрофилес..</span><span class="sxs-lookup"><span data-stu-id="9c8bd-118">For Network and Local Services, the folder is %WINDIR%\ServiceProfiles.</span></span><br/></td>
<td><span data-ttu-id="9c8bd-119">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="9c8bd-119">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="9c8bd-120">%локалаппдата%\крашдумпс</span><span class="sxs-lookup"><span data-stu-id="9c8bd-120">%LOCALAPPDATA%\CrashDumps</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c8bd-121"><strong>думпкаунт</strong></span><span class="sxs-lookup"><span data-stu-id="9c8bd-121"><strong>DumpCount</strong></span></span></td>
<td><span data-ttu-id="9c8bd-122">Максимальное число файлов дампа в папке.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-122">The maximum number of dump files in the folder.</span></span> <span data-ttu-id="9c8bd-123">Если превышено максимальное значение, самый старый файл дампа в папке будет заменен новым файлом дампа.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-123">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span></td>
<td><span data-ttu-id="9c8bd-124">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9c8bd-124">REG_DWORD</span></span></td>
<td><span data-ttu-id="9c8bd-125">10</span><span class="sxs-lookup"><span data-stu-id="9c8bd-125">10</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c8bd-126"><strong>думптипе</strong></span><span class="sxs-lookup"><span data-stu-id="9c8bd-126"><strong>DumpType</strong></span></span></td>
<td><span data-ttu-id="9c8bd-127">Укажите один из следующих типов дампа:</span><span class="sxs-lookup"><span data-stu-id="9c8bd-127">Specify one of the following dump types:</span></span>
<ul>
<li><span data-ttu-id="9c8bd-128">0: Пользовательский дамп</span><span class="sxs-lookup"><span data-stu-id="9c8bd-128">0: Custom dump</span></span></li>
<li><span data-ttu-id="9c8bd-129">1: мини-дамп</span><span class="sxs-lookup"><span data-stu-id="9c8bd-129">1: Mini dump</span></span></li>
<li><span data-ttu-id="9c8bd-130">2: полный дамп</span><span class="sxs-lookup"><span data-stu-id="9c8bd-130">2: Full dump</span></span></li>
</ul></td>
<td><span data-ttu-id="9c8bd-131">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9c8bd-131">REG_DWORD</span></span></td>
<td><span data-ttu-id="9c8bd-132">1</span><span class="sxs-lookup"><span data-stu-id="9c8bd-132">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c8bd-133"><strong>кустомдумпфлагс</strong></span><span class="sxs-lookup"><span data-stu-id="9c8bd-133"><strong>CustomDumpFlags</strong></span></span></td>
<td><span data-ttu-id="9c8bd-134">Используемые параметры пользовательского дампа.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-134">The custom dump options to be used.</span></span> <span data-ttu-id="9c8bd-135">Это значение используется, только если <strong>думптипе</strong> имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-135">This value is used only when <strong>DumpType</strong> is set to 0.</span></span><br/> <span data-ttu-id="9c8bd-136">Параметры являются побитовой комбинацией значений перечисления <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9c8bd-136">The options are a bitwise combination of the <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> enumeration values.</span></span><br/></td>
<td><span data-ttu-id="9c8bd-137">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9c8bd-137">REG_DWORD</span></span></td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> <span data-ttu-id="9c8bd-138">Аварийный дамп не собирается при установке [автоматической отладки для сбоев **приложений**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span><span class="sxs-lookup"><span data-stu-id="9c8bd-138">A crash dump is not collected when you set [automatic debugging for **application** crashes](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes).</span></span> 

<span data-ttu-id="9c8bd-139">Эти значения реестра представляют глобальные параметры.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-139">These registry values represent the global settings.</span></span> <span data-ttu-id="9c8bd-140">Кроме того, можно указать параметры для каждого приложения, которые переопределяют глобальные параметры.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-140">You can also provide per-application settings that override the global settings.</span></span> <span data-ttu-id="9c8bd-141">Чтобы создать параметр для каждого приложения, создайте новый ключ для приложения в разделе **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ отчеты об ошибках Windows \\ локалдумпс** (например, **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ отчеты об ошибках Windows \\ локалдумпс \\MyApplication.exe**).</span><span class="sxs-lookup"><span data-stu-id="9c8bd-141">To create a per-application setting, create a new key for your application under **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps** (for example, **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\Windows Error Reporting\\LocalDumps\\MyApplication.exe**).</span></span> <span data-ttu-id="9c8bd-142">Добавьте параметры дампа в раздел **MyApplication.exe** .</span><span class="sxs-lookup"><span data-stu-id="9c8bd-142">Add your dump settings under the **MyApplication.exe** key.</span></span> <span data-ttu-id="9c8bd-143">Если приложение аварийно завершает работу, WER сначала считывает глобальные параметры, а затем переопределяет все параметры с параметрами конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-143">If your application crashes, WER will first read the global settings, and then will override any of the settings with your application-specific settings.</span></span>

<span data-ttu-id="9c8bd-144">После сбоя приложения и до его завершения система проверит параметры реестра, чтобы определить, следует ли собирать локальный дамп.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-144">After an application crashes and prior to its termination, the system will check the registry settings to determine whether a local dump is to be collected.</span></span> <span data-ttu-id="9c8bd-145">После завершения сбора дампа приложение будет разрешено завершаться нормально.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-145">After the dump collection has completed, the application will be allowed to terminate normally.</span></span> <span data-ttu-id="9c8bd-146">Если приложение поддерживает восстановление, то перед вызовом функции обратного вызова восстановления производится сбор локального дампа.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-146">If the application supports recovery, the local dump is collected before the recovery callback is called.</span></span>

<span data-ttu-id="9c8bd-147">Эти дампы настраиваются и управляются независимо от остальной инфраструктуры WER.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-147">These dumps are configured and controlled independently of the rest of the WER infrastructure.</span></span> <span data-ttu-id="9c8bd-148">Можно использовать локальную коллекцию дампов, даже если средство WER отключено или пользователь отменяет отчеты об WER.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-148">You can make use of the local dump collection even if WER is disabled or if the user cancels WER reporting.</span></span> <span data-ttu-id="9c8bd-149">Локальный дамп может отличаться от дампа, отправленного в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9c8bd-149">The local dump can be different than the dump sent to Microsoft.</span></span>

 

