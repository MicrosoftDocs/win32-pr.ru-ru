---
description: Демонстрирует вызов функции ShellExecute из процесса проводника Windows.
title: 'Пример: выполнение операции в проводнике'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D307B22A-E4A3-4215-B28E-F48A721260A1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7a511f7ccc7edd218edd405de163501afd530f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985585"
---
# <a name="execute-in-explorer-sample"></a><span data-ttu-id="02b20-103">Пример: выполнение операции в проводнике</span><span class="sxs-lookup"><span data-stu-id="02b20-103">Execute In Explorer Sample</span></span>

<span data-ttu-id="02b20-104">Демонстрирует вызов функции [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) из процесса проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="02b20-104">Demonstrates how to call the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function from the Windows Explorer process.</span></span> <span data-ttu-id="02b20-105">Это полезно при запуске непривилегированного процесса из процесса с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="02b20-105">This is useful when launching an unelevated process from an elevated process.</span></span>

<span data-ttu-id="02b20-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="02b20-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="02b20-107">Требования</span><span class="sxs-lookup"><span data-stu-id="02b20-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="02b20-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="02b20-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="02b20-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="02b20-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="02b20-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="02b20-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="02b20-111">Требования</span><span class="sxs-lookup"><span data-stu-id="02b20-111">Requirements</span></span>



| <span data-ttu-id="02b20-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="02b20-112">Product</span></span>                                | <span data-ttu-id="02b20-113">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="02b20-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="02b20-114">Windows</span><span class="sxs-lookup"><span data-stu-id="02b20-114">Windows</span></span>                                | <span data-ttu-id="02b20-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02b20-115">Windows Vista</span></span>           |
| <span data-ttu-id="02b20-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="02b20-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="02b20-117">7.0</span><span class="sxs-lookup"><span data-stu-id="02b20-117">7.0</span></span>                     |



 

<span data-ttu-id="02b20-118">Дополнительные требования см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="02b20-118">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="02b20-119">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="02b20-119">Downloading the Sample</span></span>

| <span data-ttu-id="02b20-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="02b20-120">Location</span></span>      | <span data-ttu-id="02b20-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="02b20-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b20-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="02b20-122">GitHub</span></span>  | [<span data-ttu-id="02b20-123">Пример ЕксеЦинексплорер</span><span class="sxs-lookup"><span data-stu-id="02b20-123">ExecInExplorer sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ExecInExplorer) |

## <a name="building-the-sample"></a><span data-ttu-id="02b20-124">Построение образца</span><span class="sxs-lookup"><span data-stu-id="02b20-124">Building the Sample</span></span>

<span data-ttu-id="02b20-125">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="02b20-125">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="02b20-126">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="02b20-126">Running the Sample</span></span>

<span data-ttu-id="02b20-127">Инструкции по созданию образца см. в файле сведений, прилагаемом к примеру.</span><span class="sxs-lookup"><span data-stu-id="02b20-127">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



