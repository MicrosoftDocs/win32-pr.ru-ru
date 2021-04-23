---
description: Реализация расширений контекстного меню
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Реализация расширений контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105711971"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="050d9-103">Реализация расширений контекстного меню</span><span class="sxs-lookup"><span data-stu-id="050d9-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="050d9-104">Расширение пространства имен WPD поддерживает расширяемые контекстные меню (или ярлыки).</span><span class="sxs-lookup"><span data-stu-id="050d9-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="050d9-105">Это меню, которое появляется, когда пользователь щелкает правой кнопкой мыши объект, например файл или папку.</span><span class="sxs-lookup"><span data-stu-id="050d9-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="050d9-106">Некоторые приложения WPD будут использовать эти расширяемые меню для поддержки операций с содержимым на стороне устройства (или объектами, расположенными на устройстве).</span><span class="sxs-lookup"><span data-stu-id="050d9-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="050d9-107">Расширяемые контекстные меню поддерживаются интерфейсами, описанными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="050d9-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="050d9-108">Дополнительные сведения об этих интерфейсах см. в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="050d9-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="050d9-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="050d9-109">Interface</span></span>           | <span data-ttu-id="050d9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="050d9-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="050d9-111">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="050d9-111">IContextMenu</span></span>        | <span data-ttu-id="050d9-112">Оболочка Windows Vista вызывает методы в этом интерфейсе для создания или слияния нового контекстного меню с заданным объектом.</span><span class="sxs-lookup"><span data-stu-id="050d9-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="050d9-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="050d9-113">IDataObject</span></span>         | <span data-ttu-id="050d9-114">Используется для передачи массива ПИДЛ контекстного меню обработчику контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="050d9-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="050d9-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="050d9-115">IPropertySetStorage</span></span> | <span data-ttu-id="050d9-116">Этот интерфейс используется для получения свойств WPD для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="050d9-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="050d9-117">ипропертистораже</span><span class="sxs-lookup"><span data-stu-id="050d9-117">IPropertyStorage</span></span>    | <span data-ttu-id="050d9-118">Этот интерфейс также используется для извлечения свойств WPD для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="050d9-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="050d9-119">ишеллекстинит</span><span class="sxs-lookup"><span data-stu-id="050d9-119">IShellExtInit</span></span>       | <span data-ttu-id="050d9-120">Инициализирует расширения оболочки Windows Vista для контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="050d9-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="050d9-121">IStream</span><span class="sxs-lookup"><span data-stu-id="050d9-121">IStream</span></span>             | <span data-ttu-id="050d9-122">Будет предоставляться.</span><span class="sxs-lookup"><span data-stu-id="050d9-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="050d9-123">Контекстные меню для WPD реализуются так же, как и любые другие контекстные меню в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="050d9-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="050d9-124">Если вы уже реализовали обработчик контекстного меню, можно изменить существующий код таким образом, чтобы он поддерживал содержимое на стороне устройства.</span><span class="sxs-lookup"><span data-stu-id="050d9-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="050d9-125">Если вы никогда не создавали обработчик контекстного меню, см. раздел Создание обработчиков контекстного меню в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="050d9-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="050d9-126">Две точки, в которых обработчик контекстного меню WPD отличается от любого другого обработчика, находятся в регистрации обработчика и поддержке содержимого на стороне устройства.</span><span class="sxs-lookup"><span data-stu-id="050d9-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



