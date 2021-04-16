---
description: В этом примере демонстрируется декодирование различных кадров в файле GIF, чтение соответствующих метаданных для каждого кадра, составление кадров и визуализация анимации с помощью Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Пример анимированного GIF-файла WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105651568"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="7c65c-103">Пример анимированного GIF-файла WIC</span><span class="sxs-lookup"><span data-stu-id="7c65c-103">WIC animated GIF sample</span></span>

<span data-ttu-id="7c65c-104">В этом примере демонстрируется декодирование различных кадров в файле GIF, чтение соответствующих метаданных для каждого кадра, составление кадров и визуализация анимации с помощью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7c65c-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c65c-105">Требования</span><span class="sxs-lookup"><span data-stu-id="7c65c-105">Requirements</span></span>

<span data-ttu-id="7c65c-106">Этот пример имеет следующие требования.</span><span class="sxs-lookup"><span data-stu-id="7c65c-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="7c65c-107">Требование</span><span class="sxs-lookup"><span data-stu-id="7c65c-107">Requirement</span></span> | <span data-ttu-id="7c65c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7c65c-108">Value</span></span> |
|-|-|
| <span data-ttu-id="7c65c-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c65c-109">Minimum supported client</span></span> | <span data-ttu-id="7c65c-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c65c-110">Windows 7</span></span> |
| <span data-ttu-id="7c65c-111">Минимальное Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7c65c-111">Minimum Windows SDK</span></span> | <span data-ttu-id="7c65c-112">[Пакет средств разработки программного обеспечения (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c65c-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="7c65c-113">Скачивание примера</span><span class="sxs-lookup"><span data-stu-id="7c65c-113">Downloading the sample</span></span>

<span data-ttu-id="7c65c-114">Этот пример доступен на [анимированном GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)-файле WIC.</span><span class="sxs-lookup"><span data-stu-id="7c65c-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="7c65c-115">Создание примера</span><span class="sxs-lookup"><span data-stu-id="7c65c-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="7c65c-116">Использование Visual Studio (предпочтительный метод)</span><span class="sxs-lookup"><span data-stu-id="7c65c-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="7c65c-117">Откройте проводник и перейдите к каталогу.</span><span class="sxs-lookup"><span data-stu-id="7c65c-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="7c65c-118">Дважды щелкните значок файла. sln (решение), чтобы открыть файл в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7c65c-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="7c65c-119">В меню **Построение** выберите команду **Построить решение**.</span><span class="sxs-lookup"><span data-stu-id="7c65c-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="7c65c-120">Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .</span><span class="sxs-lookup"><span data-stu-id="7c65c-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="7c65c-121">Использование командной строки</span><span class="sxs-lookup"><span data-stu-id="7c65c-121">Using the command prompt</span></span>

<span data-ttu-id="7c65c-122">Построение образца с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="7c65c-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="7c65c-123">Откройте командную строку и перейдите к каталогу примеров.</span><span class="sxs-lookup"><span data-stu-id="7c65c-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="7c65c-124">Введите `msbuild WICAnimatedGif.sln`</span><span class="sxs-lookup"><span data-stu-id="7c65c-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7c65c-125">Выполнение примера</span><span class="sxs-lookup"><span data-stu-id="7c65c-125">Running the sample</span></span>

<span data-ttu-id="7c65c-126">После запуска приложения Загрузите файл образа с помощью команды **Открыть** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="7c65c-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="7c65c-127">Изменение размера окна поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c65c-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c65c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c65c-128">See also</span></span>

[<span data-ttu-id="7c65c-129">Кодек Microsoft Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="7c65c-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="7c65c-130">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="7c65c-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="7c65c-131">Ссылки</span><span class="sxs-lookup"><span data-stu-id="7c65c-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="7c65c-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="7c65c-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="7c65c-133">Примеры и примеры кода</span><span class="sxs-lookup"><span data-stu-id="7c65c-133">Samples and code examples</span></span>](-wic-samples.md)
