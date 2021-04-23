---
description: Инструментарий управления Windows (WMI) (WMI) содержит новый раздел реестра для включения или отключения функции автоматического восстановления репозитория.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Раздел реестра для конфигурации репозитория
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702002"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="e43db-103">Раздел реестра для конфигурации репозитория</span><span class="sxs-lookup"><span data-stu-id="e43db-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="e43db-104">Инструментарий управления Windows (WMI) (WMI) содержит новый раздел реестра для включения или отключения функции автоматического восстановления репозитория.</span><span class="sxs-lookup"><span data-stu-id="e43db-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="e43db-105">Дополнительные сведения о восстановлении репозитория WMI см. в статье [резервное копирование и восстановление из РЕПОЗИТОРИЯ WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="e43db-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="e43db-106">В Windows 7 поведение по умолчанию — автоматическое восстановление репозитория из резервной версии при обнаружении повреждения репозитория.</span><span class="sxs-lookup"><span data-stu-id="e43db-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="e43db-107">Инструментарий WMI предоставляет значение реестра **ауторесторинаблед** для отключения этой функции.</span><span class="sxs-lookup"><span data-stu-id="e43db-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="e43db-108">Разделы реестра для WMI находятся в реестре в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="e43db-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="e43db-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**ауторесторинаблед**</span><span class="sxs-lookup"><span data-stu-id="e43db-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="e43db-110">Позволяет пользователю определить, использовать ли репозиторий автоматического восстановления.</span><span class="sxs-lookup"><span data-stu-id="e43db-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="e43db-111">По умолчанию для этого раздела задано значение 1, а функция репозиторий автовосстановления включена.</span><span class="sxs-lookup"><span data-stu-id="e43db-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="e43db-112">Возможны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="e43db-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="e43db-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="e43db-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="e43db-114">Выключено</span><span class="sxs-lookup"><span data-stu-id="e43db-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="e43db-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="e43db-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="e43db-116">Активировано</span><span class="sxs-lookup"><span data-stu-id="e43db-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="e43db-117">Значение реестра **ауторесторинаблед** можно изменить с помощью Консоль управления ГРУППОВЫМИ политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="e43db-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="e43db-118">Дополнительные сведения см. в разделе [консоль управления групповыми политиками](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="e43db-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="e43db-119">Эта процедура содержит сведения о том, как включить или отключить репозиторий автоматического восстановления.</span><span class="sxs-lookup"><span data-stu-id="e43db-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="e43db-120">**Изменение значения по умолчанию для ключа **ауторесторинаблед** с помощью групповая политика**</span><span class="sxs-lookup"><span data-stu-id="e43db-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="e43db-121">Откройте консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="e43db-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="e43db-122">Создайте объект групповая политика (GPO).</span><span class="sxs-lookup"><span data-stu-id="e43db-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="e43db-123">Измените объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="e43db-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="e43db-124">Выберите настройки/параметры Windows/реестр.</span><span class="sxs-lookup"><span data-stu-id="e43db-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="e43db-125">Щелкните правой кнопкой мыши и выберите **создать... Реестр**.</span><span class="sxs-lookup"><span data-stu-id="e43db-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="e43db-126">Это действие представляет пользовательский интерфейс, в котором можно ввести данные реестра.</span><span class="sxs-lookup"><span data-stu-id="e43db-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="e43db-127">Выберите команду **Обновить** .</span><span class="sxs-lookup"><span data-stu-id="e43db-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="e43db-128">Выберите следующий путь к разделу реестра: **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="e43db-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="e43db-129">В поле **имя** введите **ауторесторинаблед**.</span><span class="sxs-lookup"><span data-stu-id="e43db-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="e43db-130">В поле **данные** введите 0 для отключения или 1, чтобы включить функцию репозитория автовосстановления.</span><span class="sxs-lookup"><span data-stu-id="e43db-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="e43db-131">Щелкните ОК.</span><span class="sxs-lookup"><span data-stu-id="e43db-131">Click OK.</span></span>

 

 
