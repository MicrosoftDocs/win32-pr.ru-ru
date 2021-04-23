---
description: Интерфейс IWindowsDriverUpdate2 определяет следующие свойства.
ms.assetid: ed45a833-5c28-4ddc-993c-1237f69ec63f
title: Свойства IWindowsDriverUpdate2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271e6623db073313c42a7e6dedebbd33e5eb6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542255"
---
# <a name="iwindowsdriverupdate2-properties"></a><span data-ttu-id="e5d3f-103">Свойства IWindowsDriverUpdate2</span><span class="sxs-lookup"><span data-stu-id="e5d3f-103">IWindowsDriverUpdate2 Properties</span></span>

<span data-ttu-id="e5d3f-104">Интерфейс [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5d3f-104">The [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="e5d3f-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="e5d3f-105">Property</span></span>                                                       | <span data-ttu-id="e5d3f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e5d3f-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5d3f-107">**квеидс**</span><span class="sxs-lookup"><span data-stu-id="e5d3f-107">**CveIDs**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_cveids)                 | <span data-ttu-id="e5d3f-108">Содержит коллекцию стандартных идентификаторов уязвимостей и раскрытия (CVE), связанных с обновлением.</span><span class="sxs-lookup"><span data-stu-id="e5d3f-108">Contains a collection of the Common Vulnerabilities and Exposures (CVE) identifiers that are associated with an update.</span></span> |
| [<span data-ttu-id="e5d3f-109">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="e5d3f-109">**IsPresent**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_ispresent)           | <span data-ttu-id="e5d3f-110">Возвращает логическое значение, указывающее, установлено ли обновление на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e5d3f-110">Gets a Boolean value that indicates whether an update is installed on the computer.</span></span>                                     |
| [<span data-ttu-id="e5d3f-111">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="e5d3f-111">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_rebootrequired) | <span data-ttu-id="e5d3f-112">Возвращает логическое значение, указывающее, должен ли компьютер быть перезагружен после установки или удаления обновления.</span><span class="sxs-lookup"><span data-stu-id="e5d3f-112">Gets a Boolean value that indicates whether the computer must be restarted after you install or uninstall an update.</span></span>    |



 

<span data-ttu-id="e5d3f-113">Сведения о членах, наследуемых этим интерфейсом, см. в следующем интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e5d3f-113">For information about the members inherited by this interface, see the following interface.</span></span>

-   [<span data-ttu-id="e5d3f-114">**ивиндовсдриверупдате**</span><span class="sxs-lookup"><span data-stu-id="e5d3f-114">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)

 

 



