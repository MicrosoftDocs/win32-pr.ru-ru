---
title: Параметры платформа .NET Framework по умолчанию
description: Платформа .NET Framework 4,5 по умолчанию и платформа .NET Framework 3,5 являются необязательными
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "105700975"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="b7eab-103">Платформа .NET Framework 4,5 по умолчанию и платформа .NET Framework 3,5 являются необязательными</span><span class="sxs-lookup"><span data-stu-id="b7eab-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="b7eab-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="b7eab-104">Platforms</span></span>

<span data-ttu-id="b7eab-105">**Клиенты**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="b7eab-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="b7eab-106">**Серверы**   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7eab-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="b7eab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b7eab-107">Description</span></span>

<span data-ttu-id="b7eab-108">Платформа .NET Framework 4,5 по умолчанию включена в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b7eab-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="b7eab-109">По умолчанию Windows 8 не включает .NET 3,5, но файлы для .NET 3,5 доступны на установочном носителе Windows 8 как дополнительный компонент.</span><span class="sxs-lookup"><span data-stu-id="b7eab-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="b7eab-110">Если пользователь выполняет обновление с Windows 7 до Windows 8, платформа .NET Framework 3,5 полностью включена, чтобы все приложения на компьютере продолжали работать правильно.</span><span class="sxs-lookup"><span data-stu-id="b7eab-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b7eab-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="b7eab-111">Manifestation</span></span>

<span data-ttu-id="b7eab-112">Если пользователь выполняет чистую установку Windows 8, а затем устанавливает приложения, для которых требуется платформа .NET Framework 3,5 (или 2,0), они активируют запрос на наличие необходимых файлов .NET 3,5.</span><span class="sxs-lookup"><span data-stu-id="b7eab-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="b7eab-113">Обычно недостающие файлы будут скачаны из Центр обновления Windows (после запроса разрешения), но если доступ к Центр обновления Windows невозможен, включение платформа .NET Framework 3,5 завершится ошибкой, если не указан альтернативный источник отсутствующих файлов.</span><span class="sxs-lookup"><span data-stu-id="b7eab-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="b7eab-114">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="b7eab-114">Mitigation</span></span>

<span data-ttu-id="b7eab-115">Чтобы включить платформа .NET Framework 3,5 на тестовых компьютерах с чистой установкой Windows 8, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b7eab-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="b7eab-116">Скопируйте \\ источники \\ SxS \\ из подключенной операционной системы ISO-образа сборки в dotnet35 или аналогичную папку.</span><span class="sxs-lookup"><span data-stu-id="b7eab-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="b7eab-117">Пример:</span><span class="sxs-lookup"><span data-stu-id="b7eab-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="b7eab-118">Выполните эту командную строку с правами администратора:</span><span class="sxs-lookup"><span data-stu-id="b7eab-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="b7eab-119">\\Папка SxS Sources не должна использоваться в качестве механизма распространения, так как этот механизм не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7eab-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="b7eab-120">Решение</span><span class="sxs-lookup"><span data-stu-id="b7eab-120">Solution</span></span>

<span data-ttu-id="b7eab-121">**Для потребителей:**</span><span class="sxs-lookup"><span data-stu-id="b7eab-121">**For consumers:**</span></span>

<span data-ttu-id="b7eab-122">Windows 8 включает механизм, который автоматически включает платформа .NET Framework 3,5 при попытке установить распространяемый пакет или когда установщик приложения, которому требуется .NET 3,5, вызывает распространяемый компонент.</span><span class="sxs-lookup"><span data-stu-id="b7eab-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="b7eab-123">**Для разработчиков приложений (и ИТ-администраторов):**</span><span class="sxs-lookup"><span data-stu-id="b7eab-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="b7eab-124">ИТ-администраторы могут настроить приложения .NET 3,5 для работы в .NET 3,5 или .NET 4,5 (в зависимости от того, что уже установлено).</span><span class="sxs-lookup"><span data-stu-id="b7eab-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="b7eab-125">Чтобы запустить управляемое приложение на 3,5 или 4,5, просто добавьте раздел в файл конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="b7eab-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="b7eab-126">Это гарантирует, что при установке .NET 3,5 приложение будет выполняться в .NET 3,5; в противном случае приложение будет работать на платформе .NET 4,5.</span><span class="sxs-lookup"><span data-stu-id="b7eab-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="b7eab-127">Ниже приведен пример дополнительного раздела в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b7eab-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="b7eab-128">**Для корпоративных изготовителей оборудования:**</span><span class="sxs-lookup"><span data-stu-id="b7eab-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="b7eab-129">Чтобы включить платформа .NET Framework 3,5 для сборок ИАП и для приложений, которые не имеют доступа к Центр обновления Windows:</span><span class="sxs-lookup"><span data-stu-id="b7eab-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="b7eab-130">Скопируйте \\ источники \\ SxS \\ из подключенного образа ISO сборки ОС в dotnet35 или аналогичную папку.</span><span class="sxs-lookup"><span data-stu-id="b7eab-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="b7eab-131">Пример:</span><span class="sxs-lookup"><span data-stu-id="b7eab-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="b7eab-132">Задайте параметр RegKey:</span><span class="sxs-lookup"><span data-stu-id="b7eab-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="b7eab-133">**Для предприятий:**</span><span class="sxs-lookup"><span data-stu-id="b7eab-133">**For enterprises:**</span></span>

<span data-ttu-id="b7eab-134">Для компьютеров, на которых настроено использование WSUS для обслуживания, можно задать параметр реестра, чтобы разрешить компьютеру использовать Центр обновления Windows для включения .NET 3,5 вместо WSUS (обслуживание по-прежнему выполняется из WSUS, если это сделано).</span><span class="sxs-lookup"><span data-stu-id="b7eab-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="b7eab-135">Задайте параметр RegKey:</span><span class="sxs-lookup"><span data-stu-id="b7eab-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="b7eab-136">Эту запись реестра также можно задать с помощью групповая политика (Политика локального компьютера — > Конфигурация компьютера — > система административные шаблоны->.</span><span class="sxs-lookup"><span data-stu-id="b7eab-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="b7eab-137">Выберите параметр указать параметры для установки дополнительных компонентов и восстановления компонентов.</span><span class="sxs-lookup"><span data-stu-id="b7eab-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="b7eab-138">Если вы выберете параметр Contact Центр обновления Windows напрямую, чтобы скачать содержимое исправления вместо Windows Server Update Services (WSUS), любые попытки добавить компоненты Windows (например, платформа .NET Framework 3,5) или функции восстановления запустит загрузку файлов из Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="b7eab-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="b7eab-139">Для этого параметра конечным компьютерам требуется доступ к Интернету и WU.</span><span class="sxs-lookup"><span data-stu-id="b7eab-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="b7eab-140">Нормальные операции обслуживания продолжают использовать WSUS, если они были настроены в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="b7eab-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="b7eab-141">**Примечание о настройке расположения локального источника с помощью записей реестра**</span><span class="sxs-lookup"><span data-stu-id="b7eab-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="b7eab-142">ИТ-администраторы могут задать расположение локальных источников для файлов .NET 3,5 с помощью записи реестра, чтобы пользователи могли использовать диалоговое окно "Добавление и удаление компонентов Windows" для включения компонентов с отсутствующими полезными данными без указания исходного расположения.</span><span class="sxs-lookup"><span data-stu-id="b7eab-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="b7eab-143">Значение параметра реестра можно контролировать с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="b7eab-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="b7eab-144">Эта запись реестра поддерживается:</span><span class="sxs-lookup"><span data-stu-id="b7eab-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b7eab-145">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7eab-145">Entry</span></span></th>
<th><span data-ttu-id="b7eab-146">Тип</span><span class="sxs-lookup"><span data-stu-id="b7eab-146">Type</span></span></th>
<th><span data-ttu-id="b7eab-147">Описание</span><span class="sxs-lookup"><span data-stu-id="b7eab-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7eab-148">Локальный исходный путь</span><span class="sxs-lookup"><span data-stu-id="b7eab-148">Local Source Path</span></span></td>
<td><span data-ttu-id="b7eab-149">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="b7eab-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="b7eab-150">Локальные пути к источникам, используемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7eab-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="b7eab-151">Можно указать несколько путей. они должны быть разделены символом;.</span><span class="sxs-lookup"><span data-stu-id="b7eab-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="b7eab-152">Поиск по расположениям выполняется в том порядке, в котором они указаны.</span><span class="sxs-lookup"><span data-stu-id="b7eab-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="b7eab-153">Локальные расположения, указанные в командной строке DISM, имеют приоритет над расположениями, указанными в этой записи реестра.</span><span class="sxs-lookup"><span data-stu-id="b7eab-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="b7eab-154">Расположение папок можно указать в этой записи реестра.</span><span class="sxs-lookup"><span data-stu-id="b7eab-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="b7eab-155">Формат WIM можно использовать, но путь должен указывать на WIM-файл; его не нужно подключать, например:</span><span class="sxs-lookup"><span data-stu-id="b7eab-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="b7eab-156">WIM: \\ мачине\шаре\филе.Вим: 1</span><span class="sxs-lookup"><span data-stu-id="b7eab-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="b7eab-157">Обратите внимание на 1 в конце.</span><span class="sxs-lookup"><span data-stu-id="b7eab-157">Notice the  1  at the end.</span></span> <span data-ttu-id="b7eab-158">Необходимо указать числовой индекс изображения, которое будет использоваться в WIM-файле.</span><span class="sxs-lookup"><span data-stu-id="b7eab-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="b7eab-159">Для подключенного WIM-файла исходный путь должен ссылаться на каталог Windows подключенного образа, а не на точку подключения (например:/Source: <mount_point> \Windows, а не/Source: <mount_point> ).</span><span class="sxs-lookup"><span data-stu-id="b7eab-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="b7eab-160">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7eab-160">Resources</span></span>

<dl>

[<span data-ttu-id="b7eab-161">Реализация политики на основе реестра</span><span class="sxs-lookup"><span data-stu-id="b7eab-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>