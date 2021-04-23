---
description: Демонстрирует использование интерфейса Ишелллибрари для создания приложения командной строки, предоставляющего программный доступ для проверки библиотек и файлов библиотек и управления ими.
title: 'Пример: реализация командной строки с помощью библиотеки оболочки'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5EC06E69-8AC8-4d9e-BAFC-C1AFC1294023
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9db182498791fee344061c91ea570ed770f3a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498081"
---
# <a name="shell-library-command-line-sample"></a><span data-ttu-id="faea0-103">Пример: реализация командной строки с помощью библиотеки оболочки</span><span class="sxs-lookup"><span data-stu-id="faea0-103">Shell Library Command Line Sample</span></span>

<span data-ttu-id="faea0-104">Демонстрирует использование интерфейса [**ишелллибрари**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) для создания приложения командной строки, предоставляющего программный доступ для проверки библиотек и файлов библиотек и управления ими.</span><span class="sxs-lookup"><span data-stu-id="faea0-104">Demonstrates how to use the [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) interface to create a command-line application that provides programmatic access for inspecting and manipulating libraries and library files.</span></span>

<span data-ttu-id="faea0-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="faea0-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="faea0-106">Требования</span><span class="sxs-lookup"><span data-stu-id="faea0-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="faea0-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="faea0-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="faea0-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="faea0-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="faea0-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="faea0-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="faea0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="faea0-110">Requirements</span></span>



| <span data-ttu-id="faea0-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="faea0-111">Product</span></span>                                | <span data-ttu-id="faea0-112">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="faea0-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="faea0-113">Windows</span><span class="sxs-lookup"><span data-stu-id="faea0-113">Windows</span></span>                                | <span data-ttu-id="faea0-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="faea0-114">Windows 7</span></span>               |
| <span data-ttu-id="faea0-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="faea0-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="faea0-116">7.0</span><span class="sxs-lookup"><span data-stu-id="faea0-116">7.0</span></span>                     |



 

<span data-ttu-id="faea0-117">Дополнительные требования см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="faea0-117">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="faea0-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="faea0-118">Downloading the Sample</span></span>

| <span data-ttu-id="faea0-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="faea0-119">Location</span></span>      | <span data-ttu-id="faea0-120">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="faea0-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faea0-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="faea0-121">GitHub</span></span>  | [<span data-ttu-id="faea0-122">Пример Шелллибрарикоммандлине</span><span class="sxs-lookup"><span data-stu-id="faea0-122">ShellLibraryCommandLine sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryCommandLine) |

## <a name="building-the-sample"></a><span data-ttu-id="faea0-123">Построение образца</span><span class="sxs-lookup"><span data-stu-id="faea0-123">Building the Sample</span></span>

<span data-ttu-id="faea0-124">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="faea0-124">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="faea0-125">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="faea0-125">Running the Sample</span></span>

<span data-ttu-id="faea0-126">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="faea0-126">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



