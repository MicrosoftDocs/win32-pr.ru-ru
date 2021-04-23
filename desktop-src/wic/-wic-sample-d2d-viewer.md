---
description: В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования файла изображения и Direct2D для отображения изображения на экране.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Средство просмотра изображений WIC с использованием примера Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105651567"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="4cd4d-103">Средство просмотра изображений WIC с использованием примера Direct2D</span><span class="sxs-lookup"><span data-stu-id="4cd4d-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="4cd4d-104">В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования файла изображения и Direct2D для отображения изображения на экране.</span><span class="sxs-lookup"><span data-stu-id="4cd4d-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd4d-105">Требования</span><span class="sxs-lookup"><span data-stu-id="4cd4d-105">Requirements</span></span>

<span data-ttu-id="4cd4d-106">Этот пример имеет следующие требования.</span><span class="sxs-lookup"><span data-stu-id="4cd4d-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="4cd4d-107">Требование</span><span class="sxs-lookup"><span data-stu-id="4cd4d-107">Requirement</span></span> | <span data-ttu-id="4cd4d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd4d-108">Value</span></span> |
|-|-|
| <span data-ttu-id="4cd4d-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cd4d-109">Minimum supported client</span></span> | <span data-ttu-id="4cd4d-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cd4d-110">Windows Vista</span></span> |
| <span data-ttu-id="4cd4d-111">Минимальное Windows SDK</span><span class="sxs-lookup"><span data-stu-id="4cd4d-111">Minimum Windows SDK</span></span> | <span data-ttu-id="4cd4d-112">[Пакет средств разработки программного обеспечения (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для Windows 7</span><span class="sxs-lookup"><span data-stu-id="4cd4d-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="4cd4d-113">Скачивание примера</span><span class="sxs-lookup"><span data-stu-id="4cd4d-113">Downloading the sample</span></span>

<span data-ttu-id="4cd4d-114">Этот образец доступен в [средстве просмотра WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span><span class="sxs-lookup"><span data-stu-id="4cd4d-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="4cd4d-115">Создание примера</span><span class="sxs-lookup"><span data-stu-id="4cd4d-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="4cd4d-116">Использование Visual Studio (предпочтительный метод)</span><span class="sxs-lookup"><span data-stu-id="4cd4d-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="4cd4d-117">Откройте проводник и перейдите к каталогу.</span><span class="sxs-lookup"><span data-stu-id="4cd4d-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="4cd4d-118">Дважды щелкните значок файла. sln (решение), чтобы открыть файл в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4cd4d-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="4cd4d-119">В меню **Построение** выберите команду **Построить решение**.</span><span class="sxs-lookup"><span data-stu-id="4cd4d-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="4cd4d-120">Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .</span><span class="sxs-lookup"><span data-stu-id="4cd4d-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="4cd4d-121">Использование командной строки</span><span class="sxs-lookup"><span data-stu-id="4cd4d-121">Using the command prompt</span></span>

<span data-ttu-id="4cd4d-122">Чтобы построить пример с помощью командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4cd4d-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="4cd4d-123">Откройте окно командной строки и перейдите к каталогу примеров.</span><span class="sxs-lookup"><span data-stu-id="4cd4d-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="4cd4d-124">Введите `msbuild WICViewerD2D.sln`</span><span class="sxs-lookup"><span data-stu-id="4cd4d-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4cd4d-125">Выполнение примера</span><span class="sxs-lookup"><span data-stu-id="4cd4d-125">Running the sample</span></span>

<span data-ttu-id="4cd4d-126">После запуска приложения Загрузите файл изображения с помощью команды **Открыть** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="4cd4d-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cd4d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cd4d-127">See also</span></span>

[<span data-ttu-id="4cd4d-128">Кодек Microsoft Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="4cd4d-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="4cd4d-129">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="4cd4d-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="4cd4d-130">Ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd4d-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="4cd4d-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4cd4d-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="4cd4d-132">Примеры и примеры кода</span><span class="sxs-lookup"><span data-stu-id="4cd4d-132">Samples and code examples</span></span>](-wic-samples.md)
