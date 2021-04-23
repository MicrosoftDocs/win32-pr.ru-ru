---
description: Уведомляет установщик Windows использовать диспетчер перезапуска для завершения работы всех приложений, в которых используются файлы, и для их перезапуска в конце установки.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: Рмшутдовнандрестарт таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650633"
---
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="c0a9d-103">Рмшутдовнандрестарт таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="c0a9d-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="c0a9d-104">Это событие уведомляет установщик Windows использовать [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) для завершения работы всех приложений, в которых используются файлы, и для их перезапуска в конце установки.</span><span class="sxs-lookup"><span data-stu-id="c0a9d-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="c0a9d-105">Этот таблице ControlEvent событие не действует, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="c0a9d-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="c0a9d-106">Операционной системой, в которой работает установка, не является Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c0a9d-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="c0a9d-107">Взаимодействие с [диспетчером перезапуска](../rstmgr/restart-manager-portal.md) отключено свойством [**Мсирестартманажерконтрол**](msirestartmanagercontrol.md) или политикой [дисаблеаутоматикаппликатионшутдовн](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a9d-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="c0a9d-108">В настоящее время нет открытого сеанса [диспетчера перезапуска](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a9d-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="c0a9d-109">Любые вызовы установщик Windows в [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) возвращают ошибку.</span><span class="sxs-lookup"><span data-stu-id="c0a9d-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c0a9d-110">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="c0a9d-110">Typical Use</span></span>

<span data-ttu-id="c0a9d-111">Событие элемента управления Рмшутдовнандрестарт публикуется только в элементе управления " [кнопка](pushbutton-control.md) " в [диалоговом окне мсирмфилесинусе](msirmfilesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a9d-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 
