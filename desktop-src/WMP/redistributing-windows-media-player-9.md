---
title: Распространение серии проигрывателя Windows Media 9
description: Распространение серии проигрывателя Windows Media 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068517"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="bee41-103">Распространение серии проигрывателя Windows Media 9</span><span class="sxs-lookup"><span data-stu-id="bee41-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="bee41-104">Вы можете установить Windows Media Player 9 Series в Windows XP с помощью одной из следующих программ установки.</span><span class="sxs-lookup"><span data-stu-id="bee41-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="bee41-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="bee41-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="bee41-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="bee41-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="bee41-107">MPSetup.exe является надмножеством программы установки MPSetupXP.exe.</span><span class="sxs-lookup"><span data-stu-id="bee41-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="bee41-108">Он содержит файлы, необходимые операционным системам, выпущенным до Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bee41-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="bee41-109">MPSetup.exe функционально эквивалентен MPSetupXP.exe при запуске в Windows XP, но размер файла программы установки больше, так как он не был оптимизирован для установки в операционных системах Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bee41-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="bee41-110">Вы можете установить Windows Media Player 9 Series в Windows 98 Second Edition, Windows Millennium Edition или Windows 2000 с помощью следующей программы установки.</span><span class="sxs-lookup"><span data-stu-id="bee41-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="bee41-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="bee41-111">MPSetup.exe</span></span>

<span data-ttu-id="bee41-112">Ниже приведен пример командной строки для установки без пользовательского интерфейса и запроса перезагрузки или перезапуска.</span><span class="sxs-lookup"><span data-stu-id="bee41-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="bee41-113">Параметр/P: \# e указывает, что установочный пакет проигрывателя Windows Media следует кэшировать во время установки проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bee41-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="bee41-114">Эта команда используется для управления будущими обновлениями операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bee41-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="bee41-115">Эта команда должна быть пропущена только корпоративными ИТ администраторами.</span><span class="sxs-lookup"><span data-stu-id="bee41-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="bee41-116">Единственный случай, когда параметр/P: \# e не должен включаться в командную строку, — если вы владеете целевой системой и уверены, что целевая система никогда не будет обновлена до более поздней операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bee41-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="bee41-117">Например, если выполняется установка серии проигрывателя Windows Media 9 в Windows 2000, а компьютер может быть обновлен до Windows XP, необходимо использовать параметр/P: \# e в командной строке.</span><span class="sxs-lookup"><span data-stu-id="bee41-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="bee41-118">В противном случае после установки Windows XP файлы проигрывателя Windows Media будут перезаписаны файлами для проигрывателя Windows Media для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bee41-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="bee41-119">В следующей таблице приведены дополнительные параметры, которые можно использовать с программой установки серии проигрывателя Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="bee41-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="bee41-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="bee41-120">Parameter</span></span>              | <span data-ttu-id="bee41-121">Описание</span><span class="sxs-lookup"><span data-stu-id="bee41-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee41-122">/номиграте</span><span class="sxs-lookup"><span data-stu-id="bee41-122">/NoMigrate</span></span>             | <span data-ttu-id="bee41-123">Предотвращение миграции библиотек.</span><span class="sxs-lookup"><span data-stu-id="bee41-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="bee41-124">/нестедресторе</span><span class="sxs-lookup"><span data-stu-id="bee41-124">/NestedRestore</span></span>         | <span data-ttu-id="bee41-125">Создайте вложенную точку восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="bee41-125">Create a nested system restore point.</span></span> <span data-ttu-id="bee41-126">Используйте этот параметр, если приложение создает точку восстановления системы для вложения точки восстановления проигрывателя Windows Media в точку восстановления приложения.</span><span class="sxs-lookup"><span data-stu-id="bee41-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bee41-127">/дисалловсистемресторе</span><span class="sxs-lookup"><span data-stu-id="bee41-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="bee41-128">Запретить создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="bee41-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="bee41-129">Этот флаг отключит создание точки восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="bee41-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="bee41-130">В большинстве случаев этот флаг не следует использовать для общего распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bee41-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="bee41-131">Его следует использовать только в том случае, если вы можете явно выбрать от имени конечного пользователя не поддерживать откат файлов проигрывателя Windows Media до более ранней версии проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="bee41-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="bee41-132">Этот флаг следует использовать только для корпоративного развертывания или установки изготовителя оборудования (OEM).</span><span class="sxs-lookup"><span data-stu-id="bee41-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="bee41-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="bee41-133">Notes</span></span>

-   <span data-ttu-id="bee41-134">В параметрах командной строки учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="bee41-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="bee41-135">При подавлении запроса на перезагрузку необходимо проверить раздел реестра Инсталлресулт и выполнить обработку уведомления о перезапуске в вызывающем приложении установки.</span><span class="sxs-lookup"><span data-stu-id="bee41-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="bee41-136">Проигрыватель Windows Media 9 Series также устанавливает среду выполнения формата Windows Media, поэтому нет необходимости включать пакет распространения проигрывателя Windows Media и пакет распространения среды выполнения Windows Media Format в одном пакете распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bee41-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="bee41-137">Поэтому при включении MPSetup.exe или MPSetupXP.exe в установку не нужно включать WMFdist.exe.</span><span class="sxs-lookup"><span data-stu-id="bee41-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee41-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bee41-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee41-139">**Распространение программного обеспечения проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bee41-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




