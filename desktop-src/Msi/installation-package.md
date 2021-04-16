---
description: Пакет установки содержит все сведения, необходимые установщик Windows для установки или удаления приложения или продукта, а также для запуска пользовательского интерфейса программы установки.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Пакет установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650858"
---
# <a name="installation-package"></a><span data-ttu-id="d4cf1-103">Пакет установки</span><span class="sxs-lookup"><span data-stu-id="d4cf1-103">Installation Package</span></span>

<span data-ttu-id="d4cf1-104">Пакет установки содержит все сведения, необходимые установщик Windows для установки или удаления приложения или продукта, а также для запуска пользовательского интерфейса программы установки.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="d4cf1-105">Каждый пакет установки включает MSI-файл, содержащий базу данных установки, информационный поток сводки и потоки данных для различных частей установки.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="d4cf1-106">MSI-файл может также содержать один или несколько преобразований, внутренних исходных файлов, а также внешних исходных файлов или CAB-файлов, необходимых для установки.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="d4cf1-107">Разработчики приложений должны создать установку для использования установщика.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="d4cf1-108">Поскольку установщик организует установки вокруг концепции [компонентов и компонентов](components-and-features.md)и хранит все сведения об установке в реляционной базе данных, процесс создания пакета установки в общем случае включает следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="d4cf1-109">Найдите функции, которые будут представлены пользователям.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="d4cf1-110">Упорядочите приложение по компонентам.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-110">Organize the application into components.</span></span>
-   <span data-ttu-id="d4cf1-111">Заполните базу данных установки данными.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="d4cf1-112">Проверьте пакет установки.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-112">Validate the installation package.</span></span>

<span data-ttu-id="d4cf1-113">В следующем разделе обсуждаются компоненты и функции установщика.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="d4cf1-114">Дополнительные сведения см. в разделе [компоненты и компоненты](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="d4cf1-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="d4cf1-115">Возможность выбора компонентов обычно определяется функциями приложения с точки зрения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="d4cf1-116">Рекомендуется, чтобы разработчики использовали стандартную процедуру выбора компонентов.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="d4cf1-117">Дополнительные сведения см. [в разделе Упорядочение приложений по компонентам](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="d4cf1-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="d4cf1-118">Авторы пакетов могут использовать средства создания пакетов сторонних разработчиков или редактор таблиц и установщик Windows SDK для заполнения базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="d4cf1-119">Все пакеты установки должны быть проверены на предмет внутренней согласованности.</span><span class="sxs-lookup"><span data-stu-id="d4cf1-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="d4cf1-120">Дополнительные сведения см. в разделе [Проверка пакетов](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="d4cf1-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



