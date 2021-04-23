---
title: Работа с выходами
description: Работа с выходами
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK, работа с выходами
- Расширенный формат систем (ASF), работа с выходами
- ASF (Расширенный системный формат), работа с выходами
- Расширенный формат систем (ASF), выходные номера и форматы
- ASF (Расширенный системный формат), выходные номера и форматы
- выходные числа и форматы, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788731"
---
# <a name="working-with-outputs"></a><span data-ttu-id="c85c6-109">Работа с выходами</span><span class="sxs-lookup"><span data-stu-id="c85c6-109">Working with Outputs</span></span>

<span data-ttu-id="c85c6-110">По умолчанию каждый пример, полученный из любого объекта модуля чтения, связан с номером выхода.</span><span class="sxs-lookup"><span data-stu-id="c85c6-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="c85c6-111">Каждый выходной номер соответствует потоку в ASF-файле.</span><span class="sxs-lookup"><span data-stu-id="c85c6-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="c85c6-112">Модуль чтения назначает выходные номера потокам в файле при открытии файла.</span><span class="sxs-lookup"><span data-stu-id="c85c6-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="c85c6-113">Обычно существует один выход для каждого потока в файле.</span><span class="sxs-lookup"><span data-stu-id="c85c6-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="c85c6-114">Однако если файл использует взаимное исключение, каждой группе взаимоисключающих потоков присваивается один выходной номер.</span><span class="sxs-lookup"><span data-stu-id="c85c6-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="c85c6-115">Поток, соответствующий выходному номеру взаимоисключающих потоков, определяется модулем чтения, в случае с несколькими файлами с битовой скоростью (MBR) или приложением, если вы используете ручной выбор потока.</span><span class="sxs-lookup"><span data-stu-id="c85c6-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="c85c6-116">Поскольку имя соединения, заданное в профиле, не сохраняется в файле, средство чтения создает имя соединения по умолчанию для каждого выхода, который представляет собой строковое представление номера выхода, например "1", "2", "3" и т. д.</span><span class="sxs-lookup"><span data-stu-id="c85c6-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="c85c6-117">Имена соединений позволяют приложениям и самому читателю сопоставлять выходные данные с потоками.</span><span class="sxs-lookup"><span data-stu-id="c85c6-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="c85c6-118">В файле нескольких битовых ставок несколько потоков совместно используют имя подключения.</span><span class="sxs-lookup"><span data-stu-id="c85c6-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="c85c6-119">Это не имеет значения для читателя, так как выходные свойства для каждого потока MBR идентичны.</span><span class="sxs-lookup"><span data-stu-id="c85c6-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="c85c6-120">Каждый выход имеет один или несколько поддерживаемых выходных форматов.</span><span class="sxs-lookup"><span data-stu-id="c85c6-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="c85c6-121">Формат выходных данных — это формат, в котором средство чтения использует несжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="c85c6-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="c85c6-122">Когда средство чтения открывает файл, он задает формат каждого выхода по умолчанию для подтипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c85c6-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="c85c6-123">Число и тип поддерживаемых выходных форматов определяется кодеком, который распаковывает данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c85c6-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="c85c6-124">В следующих разделах объясняется, как работать с выходами.</span><span class="sxs-lookup"><span data-stu-id="c85c6-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="c85c6-125">Выявление выходных номеров</span><span class="sxs-lookup"><span data-stu-id="c85c6-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="c85c6-126">Назначение форматов вывода</span><span class="sxs-lookup"><span data-stu-id="c85c6-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="c85c6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c85c6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c85c6-128">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="c85c6-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="c85c6-129">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="c85c6-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="c85c6-130">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="c85c6-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




