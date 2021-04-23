---
description: Свойство ФАСТОЕМ предназначено для того, чтобы позволить изготовителям оборудования сократить время, затрачиваемое на установку установщик Windows приложений для конкретного сценария.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: ФАСТОЕМ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689410"
---
# <a name="fastoem-property"></a><span data-ttu-id="cbfb9-103">ФАСТОЕМ, свойство</span><span class="sxs-lookup"><span data-stu-id="cbfb9-103">FASTOEM property</span></span>

<span data-ttu-id="cbfb9-104">Свойство **фастоем** предназначено для того, чтобы позволить изготовителям оборудования сократить время, затрачиваемое на установку установщик Windows приложений для конкретного сценария.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="cbfb9-105">Не Разрабатывайте свойство **фастоем** в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb9-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="cbfb9-106">Свойство **фастоем** применимо только в том случае, если выполняются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="cbfb9-107">Приложение устанавливается на том же томе, что и папка с исходными файлами.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="cbfb9-108">Исходные файлы удаляются после установки.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="cbfb9-109">Во время установки пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="cbfb9-110">[Уровень пользовательского интерфейса](user-interface-levels.md) — None.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="cbfb9-111">Установка выполняется в [контексте установки](installation-context.md)на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="cbfb9-112">На компьютере достаточно места для успешной установки.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="cbfb9-113">Это первое время установки.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-113">This is first time installation.</span></span> <span data-ttu-id="cbfb9-114">Установка не является рекламным, переустановкой, удалением или выполнением административной установки.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="cbfb9-115">Нет установленных компонентов для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="cbfb9-116">Пакет установки не содержит [изолированных компонентов](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb9-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="cbfb9-117">Поскольку изолированным компонентам требуется, чтобы исходные файлы оставались расположенными в источнике, свойство **фастоем** в настоящее время не может использоваться с изолированными компонентами.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="cbfb9-118">Если все предыдущие условия имеют значение true, установка свойства **фастоем** позволяет установщик Windows повысить производительность, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="cbfb9-119">Перемещение, а не копирование файлов на том же томе.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="cbfb9-120">Это не гарантирует, что все файлы будут перемещены, а не скопированы.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="cbfb9-121">Обратите внимание, что если компьютер имеет несколько жестких дисков, необходимо инициализировать свойство [**рутдриве**](rootdrive.md) в командной строке на том же диске, где находится источник установки.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="cbfb9-122">Исключите этот источник из списка источников приложения, чтобы при последующих установках или обслуживании по умолчанию были указаны источники компакт-дисков, указанные в [таблице Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb9-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="cbfb9-123">Оптимизируйте [стоимость файлов](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb9-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="cbfb9-124">Подавление сообщений о ходе выполнения, отправленных с установщик Windows клиенту.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbfb9-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbfb9-125">Remarks</span></span>

<span data-ttu-id="cbfb9-126">Поскольку сообщения о ходе выполнения не отправляются при установке **фастоем** , рекомендуется, чтобы авторы вручную записывали в раздел значение 1800 для времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="cbfb9-127">**HKLM** \\ **Программное обеспечение** \\ **Политики** \\ **Microsoft** \\ **Windows** \\ **Установщик** \\ **Время ожидания**</span><span class="sxs-lookup"><span data-stu-id="cbfb9-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="cbfb9-128">**\_ Параметр** timeout имеет тип reg.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="cbfb9-129">Чтобы отобразить размер приложения в окне "Установка и удаление программ" на панели управления Windows 2000, необходимо вручную записать значение EstimatedSize в раздел.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="cbfb9-130">**HKLM** \\ **Программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Удалить** \\ **<  Код > продукта**</span><span class="sxs-lookup"><span data-stu-id="cbfb9-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="cbfb9-131">Это тип **\_ DWORD reg** и равен размеру приложения в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="cbfb9-132">Установщик не записывает это значение автоматически.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="cbfb9-133">Используйте следующий пример командной строки, если компакт-диск, поставляемый конечным пользователям, хранит пакет установки приложения в корне компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="cbfb9-134">Обратите внимание, что метка тома в [таблице Media](media-table.md) файла MSI должна совпадать с МЕТКОЙ тома компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="cbfb9-135">**Msiexec/I C: \\ темпимаже \\package.msi/qn/Ле logfile.txt ALLUSERS = 1 фастоем = 1 дисаблероллбакк = 1 Рутдриве = C:\\**</span><span class="sxs-lookup"><span data-stu-id="cbfb9-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="cbfb9-136">Используйте следующий пример командной строки, если установочный пакет не находится в корне компакт-диска, поставляемого конечным пользователям.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="cbfb9-137">В этом случае в качестве значения свойства [**медиапаккажепас**](mediapackagepath.md) необходимо указать путь к установочному пакету.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="cbfb9-138">Метка тома в [таблице Media](media-table.md) файла MSI должна совпадать с МЕТКОЙ тома компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="cbfb9-139">В этом случае выполните приведенный ниже пример.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-139">In this case follow this example.</span></span>

<span data-ttu-id="cbfb9-140">**Msiexec/I C: \\ темпимаже \\package.msi/qn/Ле logfile.txt ALLUSERS = 1 фастоем = 1 дисаблероллбакк = 1 Медиапаккажепас = C: \\ темпимаже \\package.msi рутдриве = C:\\**</span><span class="sxs-lookup"><span data-stu-id="cbfb9-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfb9-141">Требования</span><span class="sxs-lookup"><span data-stu-id="cbfb9-141">Requirements</span></span>



| <span data-ttu-id="cbfb9-142">Требование</span><span class="sxs-lookup"><span data-stu-id="cbfb9-142">Requirement</span></span> | <span data-ttu-id="cbfb9-143">Значение</span><span class="sxs-lookup"><span data-stu-id="cbfb9-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfb9-144">Версия</span><span class="sxs-lookup"><span data-stu-id="cbfb9-144">Version</span></span><br/> | <span data-ttu-id="cbfb9-145">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cbfb9-146">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cbfb9-147">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cbfb9-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cbfb9-148">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb9-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbfb9-149">См. также</span><span class="sxs-lookup"><span data-stu-id="cbfb9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfb9-150">Свойства</span><span class="sxs-lookup"><span data-stu-id="cbfb9-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




