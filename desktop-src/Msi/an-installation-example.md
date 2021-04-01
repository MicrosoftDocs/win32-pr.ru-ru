---
description: В этом примере показано, как создать простой пакет установщик Windows, который устанавливает приложение.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Пример установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909111"
---
# <a name="an-installation-example"></a><span data-ttu-id="f457b-103">Пример установки</span><span class="sxs-lookup"><span data-stu-id="f457b-103">An Installation Example</span></span>

<span data-ttu-id="f457b-104">В этом примере показано, как создать простой пакет установщик Windows, который устанавливает приложение.</span><span class="sxs-lookup"><span data-stu-id="f457b-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="f457b-105">В примере устанавливается Блокнот, текстовый редактор, входящий в состав Windows, и несколько текстовых файлов, описывающих события и приемы в воображаемом красном приостановке.</span><span class="sxs-lookup"><span data-stu-id="f457b-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="f457b-106">Пример имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="f457b-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="f457b-107">Приложение предоставляется пользователям в виде самостоятельно устанавливаемого пакета установщик Windows, который устанавливает все необходимые файлы, ярлыки и сведения о реестре.</span><span class="sxs-lookup"><span data-stu-id="f457b-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="f457b-108">Пакет установки может предоставить пользователю мастер пользовательского интерфейса во время установки, чтобы получить сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="f457b-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="f457b-109">Во время установки пользователи могут выбирать отдельные компоненты, которые должны быть установлены для локального запуска, запуска от исходного кода или не устанавливаться.</span><span class="sxs-lookup"><span data-stu-id="f457b-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="f457b-110">Одна из функций может быть представлена пользователям как функция установки по запросу.</span><span class="sxs-lookup"><span data-stu-id="f457b-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="f457b-111">Этот же пакет удаляет приложение и все файлы приложений и данные реестра с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="f457b-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="f457b-112">Пакет готов к получению крупного обновления, включающего изменение кода продукта.</span><span class="sxs-lookup"><span data-stu-id="f457b-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="f457b-113">Для воспроизведения этого примера требуется программное средство, позволяющее создавать и изменять пустые установщик Windows базы данных.</span><span class="sxs-lookup"><span data-stu-id="f457b-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="f457b-114">Несколько средств создания пакетов доступны от независимых поставщиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f457b-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="f457b-115">Редактор баз данных установщик Windows, именуемый Orca, предоставляется в [компонентах Windows SDK для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f457b-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="f457b-116">Чтобы завершить этот пример, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f457b-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="f457b-117">Планирование установки</span><span class="sxs-lookup"><span data-stu-id="f457b-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="f457b-118">Импорт пустой базы данных</span><span class="sxs-lookup"><span data-stu-id="f457b-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="f457b-119">Указание структуры каталогов</span><span class="sxs-lookup"><span data-stu-id="f457b-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="f457b-120">Указание компонентов</span><span class="sxs-lookup"><span data-stu-id="f457b-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="f457b-121">Указание файлов и атрибутов файлов</span><span class="sxs-lookup"><span data-stu-id="f457b-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="f457b-122">Указание исходного носителя</span><span class="sxs-lookup"><span data-stu-id="f457b-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="f457b-123">Указание компонентов</span><span class="sxs-lookup"><span data-stu-id="f457b-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="f457b-124">Указание отношений Feature-Component</span><span class="sxs-lookup"><span data-stu-id="f457b-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="f457b-125">Добавление данных реестра</span><span class="sxs-lookup"><span data-stu-id="f457b-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="f457b-126">Указание сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="f457b-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="f457b-127">Указание свойств</span><span class="sxs-lookup"><span data-stu-id="f457b-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="f457b-128">Импорт Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="f457b-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="f457b-129">Импорт Инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="f457b-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="f457b-130">Импорт Админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="f457b-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="f457b-131">Импорт Админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="f457b-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="f457b-132">Импорт Адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="f457b-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="f457b-133">Добавление сводных данных</span><span class="sxs-lookup"><span data-stu-id="f457b-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="f457b-134">Импорт пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f457b-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="f457b-135">Проверка базы данных установки</span><span class="sxs-lookup"><span data-stu-id="f457b-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 



