---
description: Интерфейс Иинсталлатионжоб определяет следующие свойства.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Свойства Иинсталлатионжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810222"
---
# <a name="iinstallationjob-properties"></a><span data-ttu-id="9ee79-103">Свойства Иинсталлатионжоб</span><span class="sxs-lookup"><span data-stu-id="9ee79-103">IInstallationJob Properties</span></span>

<span data-ttu-id="9ee79-104">Интерфейс [**иинсталлатионжоб**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ee79-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="9ee79-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="9ee79-105">Property</span></span>                                            | <span data-ttu-id="9ee79-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9ee79-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ee79-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="9ee79-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="9ee79-108">Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатеинсталлер. бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) или [**иупдатеинсталлер. бегинунинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="9ee79-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="9ee79-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="9ee79-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="9ee79-110">Возвращает значение, указывающее, полностью ли обрабатывается вызов метода [**иупдатеинсталлер. бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) или [**иупдатеинсталлер. бегинунинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="9ee79-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="9ee79-111">**Обновления**</span><span class="sxs-lookup"><span data-stu-id="9ee79-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="9ee79-112">Возвращает интерфейс, содержащий доступную только для чтения коллекцию обновлений, указанных в установке или удалении.</span><span class="sxs-lookup"><span data-stu-id="9ee79-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 



