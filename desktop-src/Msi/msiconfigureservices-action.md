---
description: Действие Мсиконфигуресервицес настраивает службу для системы. Это действие запрашивает таблицы Мсисервицеконфиг и Мсисервицеконфигфаилуреактионс.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Действие Мсиконфигуресервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651220"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="2db20-104">Действие Мсиконфигуресервицес</span><span class="sxs-lookup"><span data-stu-id="2db20-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="2db20-105">Действие Мсиконфигуресервицес настраивает службу для системы.</span><span class="sxs-lookup"><span data-stu-id="2db20-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="2db20-106">Это действие запрашивает таблицы [мсисервицеконфиг](msiserviceconfig-table.md) и [мсисервицеконфигфаилуреактионс](msiserviceconfigfailureactions-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2db20-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="2db20-107">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2db20-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="2db20-108">Это действие доступно, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="2db20-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2db20-109">Службы Windows позволяют автоматически выполнять Предопределенные действия в ответ на сбой службы.</span><span class="sxs-lookup"><span data-stu-id="2db20-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="2db20-110">Для поддержки программной настройки этих **действий по восстановлению** при сбое службы [мсисервицеконфигфаилуреактионс](msiserviceconfigfailureactions-table.md) был добавлен в msi в версии MSI 5,0.</span><span class="sxs-lookup"><span data-stu-id="2db20-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="2db20-111">Однако эта функция работает не так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="2db20-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="2db20-112">Чтобы обойти эту проблему, разработчику приложения следует использовать функции **настраиваемого действия** в MSI для запуска **sc.exe** и настройки **параметров восстановления** соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="2db20-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="2db20-113">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="2db20-113">Sequence Restrictions</span></span>

<span data-ttu-id="2db20-114">Это стандартное действие должно использоваться в следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="2db20-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="2db20-115">стопсервицес</span><span class="sxs-lookup"><span data-stu-id="2db20-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="2db20-116">делетесервицес</span><span class="sxs-lookup"><span data-stu-id="2db20-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="2db20-117">Любое из следующих действий: [инсталлфилес](installfiles-action.md), [ремовефилес](removefiles-action.md), [дупликатефилес](duplicatefiles-action.md), [мовефилес](movefiles-action.md), [патчфилес](patchfiles-action.md)и [ремоведупликатефилес](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2db20-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="2db20-118">инсталлсервицес</span><span class="sxs-lookup"><span data-stu-id="2db20-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="2db20-119">мсиконфигуресервицес</span><span class="sxs-lookup"><span data-stu-id="2db20-119">MsiConfigureServices</span></span>

[<span data-ttu-id="2db20-120">стартсервицес</span><span class="sxs-lookup"><span data-stu-id="2db20-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="2db20-121">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="2db20-121">ActionData Messages</span></span>

<span data-ttu-id="2db20-122">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="2db20-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db20-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2db20-123">Remarks</span></span>

<span data-ttu-id="2db20-124">Для выполнения этого действия пользователь должен быть администратором или обладать повышенными привилегиями с разрешением на установку служб или на то, что приложение является частью управляемой установки.</span><span class="sxs-lookup"><span data-stu-id="2db20-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



