---
description: Демонстрирует, как перечислить библиотеки как контейнеры.
title: 'Пример: резервное копирование с помощью библиотеки оболочки'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986040"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="cbea8-103">Пример: резервное копирование с помощью библиотеки оболочки</span><span class="sxs-lookup"><span data-stu-id="cbea8-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="cbea8-104">Демонстрирует, как перечислить библиотеки как контейнеры.</span><span class="sxs-lookup"><span data-stu-id="cbea8-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="cbea8-105">Библиотеки — это новая парадигма хранения для файлов пользователей, которая появилась в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbea8-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="cbea8-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="cbea8-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cbea8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cbea8-107">Description</span></span>](#description)
-   [<span data-ttu-id="cbea8-108">Требования</span><span class="sxs-lookup"><span data-stu-id="cbea8-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cbea8-109">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="cbea8-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="cbea8-110">Создание примера</span><span class="sxs-lookup"><span data-stu-id="cbea8-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="cbea8-111">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="cbea8-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="cbea8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cbea8-112">Description</span></span>

<span data-ttu-id="cbea8-113">Этот пример представляет собой вымышленное приложение резервного копирования, которое показывает, как выбрать библиотеки с помощью диалогового окна "общие файлы".</span><span class="sxs-lookup"><span data-stu-id="cbea8-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="cbea8-114">Также показано, как выполнять резервное копирование библиотек с помощью обхода пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="cbea8-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbea8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cbea8-115">Requirements</span></span>



| <span data-ttu-id="cbea8-116">Продукт</span><span class="sxs-lookup"><span data-stu-id="cbea8-116">Product</span></span>                                | <span data-ttu-id="cbea8-117">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="cbea8-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="cbea8-118">Windows</span><span class="sxs-lookup"><span data-stu-id="cbea8-118">Windows</span></span>                                | <span data-ttu-id="cbea8-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbea8-119">Windows 7</span></span>               |
| <span data-ttu-id="cbea8-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="cbea8-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="cbea8-121">7.0</span><span class="sxs-lookup"><span data-stu-id="cbea8-121">7.0</span></span>                     |



 

<span data-ttu-id="cbea8-122">Дополнительные требования см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="cbea8-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="cbea8-123">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="cbea8-123">Downloading the Sample</span></span>

| <span data-ttu-id="cbea8-124">Расположение</span><span class="sxs-lookup"><span data-stu-id="cbea8-124">Location</span></span>      | <span data-ttu-id="cbea8-125">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="cbea8-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbea8-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="cbea8-126">GitHub</span></span>  | [<span data-ttu-id="cbea8-127">Пример Шелллибрарибаккуп</span><span class="sxs-lookup"><span data-stu-id="cbea8-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="cbea8-128">Построение образца</span><span class="sxs-lookup"><span data-stu-id="cbea8-128">Building the Sample</span></span>

<span data-ttu-id="cbea8-129">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="cbea8-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cbea8-130">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="cbea8-130">Running the Sample</span></span>

<span data-ttu-id="cbea8-131">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="cbea8-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



