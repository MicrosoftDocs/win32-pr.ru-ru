---
description: Диалоговое окно Мсирмфилесинусе можно создать для вывода списка процессов, которые в данный момент используют файлы, которые должны быть перезаписаны или удалены при установке.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Диалоговое окно Мсирмфилесинусе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999521"
---
# <a name="msirmfilesinuse-dialog"></a><span data-ttu-id="37f2b-103">Диалоговое окно Мсирмфилесинусе</span><span class="sxs-lookup"><span data-stu-id="37f2b-103">MsiRMFilesInUse Dialog</span></span>

<span data-ttu-id="37f2b-104">Диалоговое окно Мсирмфилесинусе можно создать для вывода списка процессов, которые в данный момент используют файлы, которые должны быть перезаписаны или удалены при установке.</span><span class="sxs-lookup"><span data-stu-id="37f2b-104">The MsiRMFilesInUse Dialog box can be authored to display a list of processes that are currently running files that need to be overwritten or deleted by the installation.</span></span> <span data-ttu-id="37f2b-105">Пользователь может выбрать один из вариантов: "автоматически закрывать приложения и перезапускать их" или "не закрывать приложения".</span><span class="sxs-lookup"><span data-stu-id="37f2b-105">The user can select between options to "Automatically close applications and restart them" or "Do not close applications.</span></span> <span data-ttu-id="37f2b-106">(Потребуется перезагрузка). Если пользователь выбирает параметр "автоматически закрывать приложения и перезапускать", можно создать элемент управления "Кнопка" в этом диалоговом окне для публикации события элемента управления Рмшутдовнандрестарт, а [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) может закрыть приложения и перезапустить их в конце установки.</span><span class="sxs-lookup"><span data-stu-id="37f2b-106">(A reboot will be required.)" If the user selects the "Automatically close applications and restart them" option, a push button control on this dialog box can be authored to publish the RMShutdownAndRestart control event and the [Restart Manager](../rstmgr/restart-manager-portal.md) can close the applications and restart them at the end of the installation.</span></span> <span data-ttu-id="37f2b-107">Это может устранить или уменьшить необходимость перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="37f2b-107">This can eliminate or reduce the need to restart the computer.</span></span> <span data-ttu-id="37f2b-108">Дополнительные сведения см. в разделе [перезагрузки системы](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="37f2b-108">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="37f2b-109">Диалоговое окно **мсирмфилесинусе** отображается во время установки, только если выполняются все перечисленные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="37f2b-109">The **MsiRMFilesInUse** dialog box is displayed during an installation only if all the following are true.</span></span> <span data-ttu-id="37f2b-110">Если любое из них имеет значение false, установщик Windows игнорирует диалоговое окно **мсирмфилесинусе** .</span><span class="sxs-lookup"><span data-stu-id="37f2b-110">When any of these are false, the Windows Installer ignores the **MsiRMFilesInUse** dialog box.</span></span>

-   <span data-ttu-id="37f2b-111">Версия установщик Windows, не более ранняя, чем версия 4,0, и операционная система, не более ранняя, чем Windows Vista или Windows Server 2008, выполняет установку.</span><span class="sxs-lookup"><span data-stu-id="37f2b-111">A Windows Installer version that is not earlier than version 4.0 and an operating system that is not earlier than Windows Vista or Windows Server 2008 is running the installation.</span></span>
-   <span data-ttu-id="37f2b-112">Используется полный [уровень пользовательского интерфейса интерфейса пользователя](user-interface-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="37f2b-112">The Full UI [user interface level](user-interface-levels.md) is used.</span></span>
-   <span data-ttu-id="37f2b-113">Взаимодействие с [диспетчером перезапуска](../rstmgr/restart-manager-portal.md) не было отключено свойством [**Мсирестартманажерконтрол**](msirestartmanagercontrol.md) или политикой [дисаблеаутоматикаппликатионшутдовн](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="37f2b-113">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have not been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="37f2b-114">В установочном пакете появится диалоговое окно **мсирмфилесинусе** .</span><span class="sxs-lookup"><span data-stu-id="37f2b-114">The **MsiRMFilesInUse** dialog box is present in the installation package.</span></span>
-   <span data-ttu-id="37f2b-115">Все вызовы от установщик Windows к [диспетчеру перезапуска](../rstmgr/restart-manager-portal.md) успешно выполнены.</span><span class="sxs-lookup"><span data-stu-id="37f2b-115">All calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) are successful.</span></span>

<span data-ttu-id="37f2b-116">Это диалоговое окно будет создано по мере необходимости в [действии инсталлвалидате](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="37f2b-116">This dialog box will be created as required by the [InstallValidate action](installvalidate-action.md).</span></span>

 

 
