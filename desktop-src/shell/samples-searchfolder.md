---
description: Демонстрирует создание поиска с ограничениями запросов с помощью модели программирования оболочки.
title: 'Пример: поиск в папке'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265465"
---
# <a name="search-folder-sample"></a><span data-ttu-id="13ead-103">Пример: поиск в папке</span><span class="sxs-lookup"><span data-stu-id="13ead-103">Search Folder Sample</span></span>

<span data-ttu-id="13ead-104">Демонстрирует создание поиска с ограничениями запросов с помощью модели программирования оболочки.</span><span class="sxs-lookup"><span data-stu-id="13ead-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="13ead-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="13ead-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="13ead-106">Описание</span><span class="sxs-lookup"><span data-stu-id="13ead-106">Description</span></span>](#description)
-   [<span data-ttu-id="13ead-107">Требования</span><span class="sxs-lookup"><span data-stu-id="13ead-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="13ead-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="13ead-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="13ead-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="13ead-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="13ead-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="13ead-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="13ead-111">Описание</span><span class="sxs-lookup"><span data-stu-id="13ead-111">Description</span></span>

<span data-ttu-id="13ead-112">В этом примере показано, как создать ограниченный Поиск с помощью интерфейса [**исеарчфолдеритемфактори**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) для создания элемента оболочки папки (контейнера), представляющего запрос.</span><span class="sxs-lookup"><span data-stu-id="13ead-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="13ead-113">Результаты отображаются с помощью диалогового окна открытия файла.</span><span class="sxs-lookup"><span data-stu-id="13ead-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ead-114">Требования</span><span class="sxs-lookup"><span data-stu-id="13ead-114">Requirements</span></span>



| <span data-ttu-id="13ead-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="13ead-115">Product</span></span>                                | <span data-ttu-id="13ead-116">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="13ead-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="13ead-117">Windows</span><span class="sxs-lookup"><span data-stu-id="13ead-117">Windows</span></span>                                | <span data-ttu-id="13ead-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13ead-118">Windows Vista</span></span>           |
| <span data-ttu-id="13ead-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="13ead-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="13ead-120">7.0</span><span class="sxs-lookup"><span data-stu-id="13ead-120">7.0</span></span>                     |



 

<span data-ttu-id="13ead-121">Дополнительные требования см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="13ead-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="13ead-122">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="13ead-122">Downloading the Sample</span></span>

| <span data-ttu-id="13ead-123">Расположение</span><span class="sxs-lookup"><span data-stu-id="13ead-123">Location</span></span>      | <span data-ttu-id="13ead-124">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="13ead-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ead-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="13ead-125">GitHub</span></span>  | [<span data-ttu-id="13ead-126">Пример Сеарчфолдер</span><span class="sxs-lookup"><span data-stu-id="13ead-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="13ead-127">Построение образца</span><span class="sxs-lookup"><span data-stu-id="13ead-127">Building the Sample</span></span>

<span data-ttu-id="13ead-128">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="13ead-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="13ead-129">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="13ead-129">Running the Sample</span></span>

<span data-ttu-id="13ead-130">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="13ead-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



