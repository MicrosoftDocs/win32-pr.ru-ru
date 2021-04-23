---
description: В примере кода Всфромскрипт показано, как запрашивать Поиск Windows из скрипта Microsoft Visual Basic с помощью Microsoft объекты данных ActiveX (ADO).
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: всфромскрипт
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342972"
---
# <a name="wsfromscript"></a><span data-ttu-id="83c85-103">всфромскрипт</span><span class="sxs-lookup"><span data-stu-id="83c85-103">WSFromScript</span></span>

<span data-ttu-id="83c85-104">В примере кода Всфромскрипт показано, как запрашивать Поиск Windows из скрипта Microsoft Visual Basic с помощью Microsoft объекты данных ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="83c85-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="83c85-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="83c85-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="83c85-106">Требования</span><span class="sxs-lookup"><span data-stu-id="83c85-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="83c85-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="83c85-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="83c85-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="83c85-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="83c85-109">См. также</span><span class="sxs-lookup"><span data-stu-id="83c85-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="83c85-110">Требования</span><span class="sxs-lookup"><span data-stu-id="83c85-110">Requirements</span></span>

| <span data-ttu-id="83c85-111">Продукт</span><span class="sxs-lookup"><span data-stu-id="83c85-111">Product</span></span>     | <span data-ttu-id="83c85-112">Версия продукта</span><span class="sxs-lookup"><span data-stu-id="83c85-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="83c85-113">Windows</span><span class="sxs-lookup"><span data-stu-id="83c85-113">Windows</span></span>     | <span data-ttu-id="83c85-114">Windows 7, 8.1 или 10</span><span class="sxs-lookup"><span data-stu-id="83c85-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="83c85-115">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="83c85-115">Windows SDK</span></span> | <span data-ttu-id="83c85-116">7,0 или выше</span><span class="sxs-lookup"><span data-stu-id="83c85-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="83c85-117">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="83c85-117">Downloading the Sample</span></span>

<span data-ttu-id="83c85-118">Этот пример доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="83c85-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="83c85-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="83c85-119">Location</span></span>      | <span data-ttu-id="83c85-120">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="83c85-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="83c85-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="83c85-121">GitHub</span></span>  | [<span data-ttu-id="83c85-122">Пример Всфромскрипт</span><span class="sxs-lookup"><span data-stu-id="83c85-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="83c85-123">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="83c85-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="83c85-124">Построение образца</span><span class="sxs-lookup"><span data-stu-id="83c85-124">Building the Sample</span></span>

<span data-ttu-id="83c85-125">Чтобы построить образец из окна командной строки:</span><span class="sxs-lookup"><span data-stu-id="83c85-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="83c85-126">Откройте окно командной строки и перейдите в каталог проекта **куереверисинг** .</span><span class="sxs-lookup"><span data-stu-id="83c85-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="83c85-127">Например, полный путь установки по умолчанию для пакета SDK для Windows 7 — `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` .</span><span class="sxs-lookup"><span data-stu-id="83c85-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="83c85-128">Введите `cscript QueryEverything.vbs`.</span><span class="sxs-lookup"><span data-stu-id="83c85-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83c85-129">См. также</span><span class="sxs-lookup"><span data-stu-id="83c85-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="83c85-130">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="83c85-130">Conceptual</span></span>

<span data-ttu-id="83c85-131">[**Справочник по языку VBScript**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="83c85-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="83c85-132">Другие примеры</span><span class="sxs-lookup"><span data-stu-id="83c85-132">Other Samples</span></span>

[<span data-ttu-id="83c85-133">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="83c85-133">Search Code Samples</span></span>](-search-samples-ovw.md)
