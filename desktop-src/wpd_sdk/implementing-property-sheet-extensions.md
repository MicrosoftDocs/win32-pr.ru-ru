---
description: Реализация расширений страницы свойств
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Реализация расширений страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713051"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="90bf8-103">Реализация расширений страницы свойств</span><span class="sxs-lookup"><span data-stu-id="90bf8-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="90bf8-104">Расширение пространства имен WPD поддерживает вкладки расширяемых свойств.</span><span class="sxs-lookup"><span data-stu-id="90bf8-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="90bf8-105">Это диалоговые окна свойств, которые появляются, когда пользователь щелкает правой кнопкой мыши объект, например файл или папку, и выбирает **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="90bf8-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="90bf8-106">Некоторые приложения WPD будут использовать эти расширяемые вкладки свойств для вывода свойств содержимого на стороне устройства (или объектов, которые находятся на устройстве).</span><span class="sxs-lookup"><span data-stu-id="90bf8-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="90bf8-107">Расширяемые вкладки свойств поддерживаются интерфейсами, описанными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="90bf8-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="90bf8-108">Дополнительные сведения об этих интерфейсах см. в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="90bf8-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="90bf8-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="90bf8-109">Interface</span></span>           | <span data-ttu-id="90bf8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="90bf8-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="90bf8-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="90bf8-111">IDataObject</span></span>         | <span data-ttu-id="90bf8-112">Используется для передачи массива ПИДЛ контекстного меню обработчику контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="90bf8-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="90bf8-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="90bf8-113">IPropertySetStorage</span></span> | <span data-ttu-id="90bf8-114">Этот интерфейс используется для получения свойств WPD для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="90bf8-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="90bf8-115">ипропертистораже</span><span class="sxs-lookup"><span data-stu-id="90bf8-115">IPropertyStorage</span></span>    | <span data-ttu-id="90bf8-116">Этот интерфейс также используется для извлечения свойств WPD для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="90bf8-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="90bf8-117">ишеллекстинит</span><span class="sxs-lookup"><span data-stu-id="90bf8-117">IShellExtInit</span></span>       | <span data-ttu-id="90bf8-118">Инициализирует расширения оболочки Windows Vista для контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="90bf8-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="90bf8-119">ишеллпропшитекст</span><span class="sxs-lookup"><span data-stu-id="90bf8-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="90bf8-120">Поддерживает добавление расширений вкладки свойств.</span><span class="sxs-lookup"><span data-stu-id="90bf8-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="90bf8-121">Вкладки свойств для WPD реализованы как любые другие вкладки свойств в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90bf8-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="90bf8-122">Если вы уже реализовали обработчик страницы свойств, можно изменить существующий код таким образом, чтобы он поддерживал содержимое на стороне устройства.</span><span class="sxs-lookup"><span data-stu-id="90bf8-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="90bf8-123">Если вы никогда не создавали обработчик контекстного меню, см. раздел Создание обработчиков страницы свойств в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="90bf8-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="90bf8-124">Две точки, в которых обработчик страницы свойств WPD отличается от любого другого обработчика, находятся в регистрации обработчика и поддержке содержимого на стороне устройства.</span><span class="sxs-lookup"><span data-stu-id="90bf8-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



