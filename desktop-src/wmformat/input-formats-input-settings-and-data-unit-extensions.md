---
title: Форматы ввода, параметры ввода и модули данных
description: Форматы ввода, параметры ввода и модули данных
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media Format SDK, форматы входных данных и параметры
- Windows Media Format SDK, расширения модулей данных
- Windows Media Format SDK, системы расширений полезных данных
- Расширенный формат систем (ASF), форматы входных данных и параметры
- ASF (Расширенный системный формат), форматы входных данных и параметры
- Расширенный системный формат (ASF), расширения модулей данных
- ASF (Расширенный системный формат), расширения модулей данных
- Расширенные системные форматы (ASF), системы расширения полезных данных
- ASF (Расширенный системный формат), системы расширения полезных данных
- расширения модулей данных, сведения
- системы расширения полезных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986719"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="c00a2-114">Форматы ввода, параметры ввода и модули данных</span><span class="sxs-lookup"><span data-stu-id="c00a2-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="c00a2-115">Объект модуля записи поддерживает входные параметры, форматы ввода и расширения модулей данных, позволяющие управлять функциями модуля записи.</span><span class="sxs-lookup"><span data-stu-id="c00a2-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="c00a2-116">Не всегда очевидно, какие методы используются для управления определенной функцией.</span><span class="sxs-lookup"><span data-stu-id="c00a2-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="c00a2-117">Форматы входных данных — это форматы мультимедиа, описывающие основные свойства носителя, который передается в модуль записи для кодирования.</span><span class="sxs-lookup"><span data-stu-id="c00a2-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="c00a2-118">Например, размер кадра и цветовое пространство для входного видео описываются в формате входных данных.</span><span class="sxs-lookup"><span data-stu-id="c00a2-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="c00a2-119">Входные параметры — это характеристики входных данных, которые выходят за пределы основ, или сведения о преобразованиях, выполняемых с данными.</span><span class="sxs-lookup"><span data-stu-id="c00a2-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="c00a2-120">Примерами входных параметров являются параметры видео с чередованием и сведения о системе водяных знаков.</span><span class="sxs-lookup"><span data-stu-id="c00a2-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="c00a2-121">Модули обработки данных, также называемые системами расширения полезной нагрузки, — это значения, которые присоединяются к отдельным образцам в разделе данных файла.</span><span class="sxs-lookup"><span data-stu-id="c00a2-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="c00a2-122">Коды времени SMPTE и неквадратные сведения о точках являются примерами модулей обработки данных.</span><span class="sxs-lookup"><span data-stu-id="c00a2-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c00a2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c00a2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c00a2-124">**Настройка расширений модуля данных**</span><span class="sxs-lookup"><span data-stu-id="c00a2-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="c00a2-125">**Расширения модулей данных**</span><span class="sxs-lookup"><span data-stu-id="c00a2-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="c00a2-126">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="c00a2-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="c00a2-127">**Перечисление формата входных данных**</span><span class="sxs-lookup"><span data-stu-id="c00a2-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="c00a2-128">**Входные параметры**</span><span class="sxs-lookup"><span data-stu-id="c00a2-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="c00a2-129">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="c00a2-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




