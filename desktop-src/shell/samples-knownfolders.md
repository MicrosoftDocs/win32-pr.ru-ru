---
description: Демонстрирует, как определить, зарегистрировать, перечислить и найти путь для всех известных папок в текущей системе.
title: 'Пример: известные папки'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 49799A9E-BA86-4977-B5F3-590BE1E5FBF6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d3784e64986a338f6554534199852191bd06ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998756"
---
# <a name="known-folders-sample"></a><span data-ttu-id="a5497-103">Пример: известные папки</span><span class="sxs-lookup"><span data-stu-id="a5497-103">Known Folders Sample</span></span>

<span data-ttu-id="a5497-104">Демонстрирует, как определить, зарегистрировать, перечислить и найти путь для всех известных папок в текущей системе.</span><span class="sxs-lookup"><span data-stu-id="a5497-104">Demonstrates how to define, register, enumerate and find the path for all known folders on the current system.</span></span>

<span data-ttu-id="a5497-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="a5497-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a5497-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a5497-106">Description</span></span>](#description)
-   [<span data-ttu-id="a5497-107">Требования</span><span class="sxs-lookup"><span data-stu-id="a5497-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a5497-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a5497-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a5497-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="a5497-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a5497-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a5497-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="a5497-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a5497-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="a5497-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a5497-112">Description</span></span>

<span data-ttu-id="a5497-113">Этот пример включает файл реестра, в котором показано, как зарегистрировать известную папку, записав некоторые общие разделы реестра и значения для разработчиков, которые предпочитают доступ к реестру.</span><span class="sxs-lookup"><span data-stu-id="a5497-113">This sample includes a registry file that demonstrates how to register a known folder by writing some common registry keys and values for developers who prefer registry access.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5497-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a5497-114">Requirements</span></span>



| <span data-ttu-id="a5497-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="a5497-115">Product</span></span>                                | <span data-ttu-id="a5497-116">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="a5497-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a5497-117">Windows</span><span class="sxs-lookup"><span data-stu-id="a5497-117">Windows</span></span>                                | <span data-ttu-id="a5497-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5497-118">Windows Vista</span></span>           |
| <span data-ttu-id="a5497-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a5497-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a5497-120">6.1</span><span class="sxs-lookup"><span data-stu-id="a5497-120">6.1</span></span>                     |



 

<span data-ttu-id="a5497-121">Дополнительные требования см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="a5497-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a5497-122">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a5497-122">Downloading the Sample</span></span>

| <span data-ttu-id="a5497-123">Расположение</span><span class="sxs-lookup"><span data-stu-id="a5497-123">Location</span></span>      | <span data-ttu-id="a5497-124">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="a5497-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5497-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="a5497-125">GitHub</span></span>  | [<span data-ttu-id="a5497-126">Пример Кновнфолдерс</span><span class="sxs-lookup"><span data-stu-id="a5497-126">KnownFolders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/knownfolders) |

## <a name="building-the-sample"></a><span data-ttu-id="a5497-127">Построение образца</span><span class="sxs-lookup"><span data-stu-id="a5497-127">Building the Sample</span></span>

<span data-ttu-id="a5497-128">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="a5497-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a5497-129">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a5497-129">Running the Sample</span></span>

<span data-ttu-id="a5497-130">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="a5497-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5497-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a5497-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5497-132">Известные папки</span><span class="sxs-lookup"><span data-stu-id="a5497-132">Known Folders</span></span>](known-folders.md)
</dt> </dl>

 

 



