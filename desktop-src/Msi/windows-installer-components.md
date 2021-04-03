---
description: Компонент — это часть приложения или продукта для установки.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Компоненты установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998791"
---
# <a name="windows-installer-components"></a><span data-ttu-id="1db40-103">Компоненты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="1db40-103">Windows Installer Components</span></span>

<span data-ttu-id="1db40-104">Компонент — это часть приложения или продукта для установки.</span><span class="sxs-lookup"><span data-stu-id="1db40-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="1db40-105">Примеры компонентов включают в себя отдельные файлы, группу связанных файлов, объекты COM, регистрацию, разделы реестра, ярлыки, ресурсы, библиотеки, сгруппированные в каталог, или общие фрагменты кода, такие как MFC или DAO.</span><span class="sxs-lookup"><span data-stu-id="1db40-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="1db40-106">Служба установщика устанавливает или удаляет компонент в виде одной согласованной части.</span><span class="sxs-lookup"><span data-stu-id="1db40-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="1db40-107">Он отслеживает каждый компонент по соответствующему идентификатору GUID компонента, указанному в столбце ComponentId [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="1db40-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="1db40-108">Два компонента, совместно использующих один и тот же идентификатор компонента, обрабатываются как несколько экземпляров одного и того же компонента независимо от их фактического содержимого.</span><span class="sxs-lookup"><span data-stu-id="1db40-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="1db40-109">На компьютере пользователя устанавливается только один экземпляр любого компонента.</span><span class="sxs-lookup"><span data-stu-id="1db40-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="1db40-110">Поэтому некоторые функции или приложения могут совместно использовать некоторые компоненты.</span><span class="sxs-lookup"><span data-stu-id="1db40-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="1db40-111">Поскольку компоненты обычно являются общими, автор пакета установки должен следовать стандартным правилам при указании компонентов функции или приложения.</span><span class="sxs-lookup"><span data-stu-id="1db40-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="1db40-112">Это важно для правильной работы механизма подсчета ссылок установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="1db40-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="1db40-113">Дополнительные сведения см. [в разделе Упорядочение приложений по компонентам](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="1db40-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="1db40-114">Вкратце, следующие правила:</span><span class="sxs-lookup"><span data-stu-id="1db40-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="1db40-115">Каждый компонент должен храниться в одной папке.</span><span class="sxs-lookup"><span data-stu-id="1db40-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="1db40-116">Ни один из файлов, запись реестра, ярлык или другие ресурсы никогда не будут поставляться как член более чем одного компонента.</span><span class="sxs-lookup"><span data-stu-id="1db40-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="1db40-117">Это распространяется на продукты, версии продуктов и компании.</span><span class="sxs-lookup"><span data-stu-id="1db40-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="1db40-118">Дополнительные сведения об использовании компонентов см. в разделе.</span><span class="sxs-lookup"><span data-stu-id="1db40-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="1db40-119">Установка отсутствующего компонента</span><span class="sxs-lookup"><span data-stu-id="1db40-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="1db40-120">Установка постоянных компонентов, файлов, шрифтов, разделов реестра</span><span class="sxs-lookup"><span data-stu-id="1db40-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="1db40-121">Использование полных компонентов</span><span class="sxs-lookup"><span data-stu-id="1db40-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="1db40-122">Использование транзитивных компонентов</span><span class="sxs-lookup"><span data-stu-id="1db40-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="1db40-123">Работа с функциями и компонентами</span><span class="sxs-lookup"><span data-stu-id="1db40-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="1db40-124">Создание большого пакета</span><span class="sxs-lookup"><span data-stu-id="1db40-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="1db40-125">Проверка установки компонентов, компонентов, файлов</span><span class="sxs-lookup"><span data-stu-id="1db40-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="1db40-126">Поиск неработающей функции или компонента</span><span class="sxs-lookup"><span data-stu-id="1db40-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="1db40-127">Публикация продуктов, компонентов и компонентов</span><span class="sxs-lookup"><span data-stu-id="1db40-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 



