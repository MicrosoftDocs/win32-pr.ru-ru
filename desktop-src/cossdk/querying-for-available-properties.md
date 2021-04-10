---
description: Запрос доступных свойств
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Запрос доступных свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142379"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="43d10-103">Запрос доступных свойств</span><span class="sxs-lookup"><span data-stu-id="43d10-103">Querying for Available Properties</span></span>

<span data-ttu-id="43d10-104">При написании средства администрирования общего назначения вам, скорее всего, придется написать подпрограммы для настройки свойств в полной общей настройке.</span><span class="sxs-lookup"><span data-stu-id="43d10-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="43d10-105">Для этого существует средство, которое позволяет динамически запрашивать свойства, доступные для элементов в любой заданной коллекции.</span><span class="sxs-lookup"><span data-stu-id="43d10-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="43d10-106">Коллекция [**PropertyInfo**](propertyinfo.md) доступна из любой коллекции, которую вы можете удерживать.</span><span class="sxs-lookup"><span data-stu-id="43d10-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="43d10-107">Коллекция **PropertyInfo** содержит элемент для каждого доступного свойства.</span><span class="sxs-lookup"><span data-stu-id="43d10-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="43d10-108">Можно перечислить эти элементы, чтобы определить, доступно ли данное свойство.</span><span class="sxs-lookup"><span data-stu-id="43d10-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="43d10-109">Коллекцию [**PropertyInfo**](propertyinfo.md) можно получить из любой коллекции, которую вы удерживаете, используя метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , и оставить второй параметр пустым, где обычно указывается свойство ключа родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="43d10-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43d10-110">См. также</span><span class="sxs-lookup"><span data-stu-id="43d10-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43d10-111">Получение и задание свойств</span><span class="sxs-lookup"><span data-stu-id="43d10-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="43d10-112">Взаимозависимости между свойствами</span><span class="sxs-lookup"><span data-stu-id="43d10-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="43d10-113">Сохранение или Отмена изменений</span><span class="sxs-lookup"><span data-stu-id="43d10-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



