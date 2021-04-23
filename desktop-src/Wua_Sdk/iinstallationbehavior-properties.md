---
description: Интерфейс Иинсталлатионбехавиор определяет следующие свойства.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Свойства Иинсталлатионбехавиор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991172"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="abc77-103">Свойства Иинсталлатионбехавиор</span><span class="sxs-lookup"><span data-stu-id="abc77-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="abc77-104">Интерфейс [**иинсталлатионбехавиор**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="abc77-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="abc77-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="abc77-105">Property</span></span>                                                                                 | <span data-ttu-id="abc77-106">Описание</span><span class="sxs-lookup"><span data-stu-id="abc77-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abc77-107">**канрекуестусеринпут**</span><span class="sxs-lookup"><span data-stu-id="abc77-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="abc77-108">Возвращает логическое значение САСТ, указывающее, может ли установка или удаление обновления запрашивать ввод данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="abc77-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="abc77-109">**Влияние**</span><span class="sxs-lookup"><span data-stu-id="abc77-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="abc77-110">Возвращает перечисление [**инсталлатионимпакт**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) , которое указывает, как установка или удаление обновления затрагивает компьютер.</span><span class="sxs-lookup"><span data-stu-id="abc77-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="abc77-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="abc77-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="abc77-112">Возвращает перечисление [**инсталлатионребутбехавиор**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) , указывающее поведение при перезапуске, которое происходит при установке или удалении обновления.</span><span class="sxs-lookup"><span data-stu-id="abc77-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="abc77-113">**рекуиреснетворкконнективити**</span><span class="sxs-lookup"><span data-stu-id="abc77-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="abc77-114">Возвращает логическое значение, указывающее, требуется ли сетевое подключение для установки или удаления обновления.</span><span class="sxs-lookup"><span data-stu-id="abc77-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 



