---
description: В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования изображения, закодированного с помощью последовательных уровней.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Пример прогрессивного декодирования компонента WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105714073"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="e2d65-103">Пример прогрессивного декодирования компонента WIC</span><span class="sxs-lookup"><span data-stu-id="e2d65-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="e2d65-104">В этом примере демонстрируется использование компонента Windows Imaging Component (WIC) для декодирования изображения, закодированного с помощью последовательных уровней.</span><span class="sxs-lookup"><span data-stu-id="e2d65-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="e2d65-105">В этом примере используется Direct2D для отображения различных последовательных уровней на экране.</span><span class="sxs-lookup"><span data-stu-id="e2d65-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d65-106">Требования</span><span class="sxs-lookup"><span data-stu-id="e2d65-106">Requirements</span></span>

<span data-ttu-id="e2d65-107">Этот пример имеет следующие требования.</span><span class="sxs-lookup"><span data-stu-id="e2d65-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="e2d65-108">Требование</span><span class="sxs-lookup"><span data-stu-id="e2d65-108">Requirement</span></span> | <span data-ttu-id="e2d65-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e2d65-109">Value</span></span> |
|-|
| <span data-ttu-id="e2d65-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2d65-110">Minimum supported client</span></span> | <span data-ttu-id="e2d65-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2d65-111">Windows 7</span></span> |
| <span data-ttu-id="e2d65-112">Минимальное Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e2d65-112">Minimum Windows SDK</span></span> | <span data-ttu-id="e2d65-113">[Пакет средств разработки программного обеспечения (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) для Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2d65-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="e2d65-114">Скачивание примера</span><span class="sxs-lookup"><span data-stu-id="e2d65-114">Downloading the sample</span></span>

<span data-ttu-id="e2d65-115">Этот пример доступен в [прогрессивной кодировке WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span><span class="sxs-lookup"><span data-stu-id="e2d65-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="e2d65-116">Создание примера</span><span class="sxs-lookup"><span data-stu-id="e2d65-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="e2d65-117">Использование Visual Studio (предпочтительный метод)</span><span class="sxs-lookup"><span data-stu-id="e2d65-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="e2d65-118">Откройте проводник и перейдите к каталогу.</span><span class="sxs-lookup"><span data-stu-id="e2d65-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="e2d65-119">Дважды щелкните значок файла. sln (решение), чтобы открыть файл в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e2d65-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="e2d65-120">В меню Построение выберите команду Построить решение.</span><span class="sxs-lookup"><span data-stu-id="e2d65-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="e2d65-121">Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .</span><span class="sxs-lookup"><span data-stu-id="e2d65-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="e2d65-122">Использование командной строки</span><span class="sxs-lookup"><span data-stu-id="e2d65-122">Using the command prompt</span></span>

<span data-ttu-id="e2d65-123">Для построения примера с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="e2d65-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="e2d65-124">Откройте командную строку и перейдите к каталогу примеров.</span><span class="sxs-lookup"><span data-stu-id="e2d65-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="e2d65-125">Введите `msbuild WICProgressiveDecoding.sln`</span><span class="sxs-lookup"><span data-stu-id="e2d65-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e2d65-126">Выполнение примера</span><span class="sxs-lookup"><span data-stu-id="e2d65-126">Running the sample</span></span>

<span data-ttu-id="e2d65-127">После запуска приложения Загрузите файл изображения через меню открыть файл.</span><span class="sxs-lookup"><span data-stu-id="e2d65-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="e2d65-128">При загрузке для последовательного уровня по умолчанию устанавливается значение 0.</span><span class="sxs-lookup"><span data-stu-id="e2d65-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="e2d65-129">Переход к различным последовательным уровням можно осуществлять с помощью меню или клавиши со стрелками вверх или вниз.</span><span class="sxs-lookup"><span data-stu-id="e2d65-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="e2d65-130">Текущий текст последовательного уровня отображается в строке состояния главного окна.</span><span class="sxs-lookup"><span data-stu-id="e2d65-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="e2d65-131">Изменение размера окна поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2d65-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="e2d65-132">Прогрессивное декодирование доступно только для образов с последовательной кодировкой.</span><span class="sxs-lookup"><span data-stu-id="e2d65-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="e2d65-133">Образ, предоставленный в этом примере, был постепенно закодирован.</span><span class="sxs-lookup"><span data-stu-id="e2d65-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2d65-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2d65-134">See also</span></span>

[<span data-ttu-id="e2d65-135">Кодек Microsoft Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="e2d65-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="e2d65-136">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="e2d65-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="e2d65-137">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e2d65-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="e2d65-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="e2d65-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="e2d65-139">Примеры и примеры кода</span><span class="sxs-lookup"><span data-stu-id="e2d65-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="e2d65-140">Обзор прогрессивного декодирования</span><span class="sxs-lookup"><span data-stu-id="e2d65-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
