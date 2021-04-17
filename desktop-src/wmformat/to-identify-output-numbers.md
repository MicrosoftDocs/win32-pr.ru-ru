---
title: Выявление выходных номеров
description: Выявление выходных номеров
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, идентифицирующие выходные номера
- Расширенный системный формат (ASF), идентифицирующие выходные номера
- ASF (Расширенный системный формат), определение выходных номеров
- Расширенный формат систем (ASF), выходные номера и форматы
- ASF (Расширенный системный формат), выходные номера и форматы
- выходные числа и форматы, определение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710233"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="385c2-109">Выявление выходных номеров</span><span class="sxs-lookup"><span data-stu-id="385c2-109">To Identify Output Numbers</span></span>

<span data-ttu-id="385c2-110">Чтобы узнать выходные номера загруженного файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="385c2-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="385c2-111">Эти процедуры идентичны как для асинхронного чтения, так и для синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="385c2-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="385c2-112">Если имена интерфейсов различаются, методы синхронного чтения перечисляются в скобках после методов асинхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="385c2-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="385c2-113">Создайте объект Reader и загрузите файл для чтения.</span><span class="sxs-lookup"><span data-stu-id="385c2-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="385c2-114">Дополнительные сведения см. [в разделе Создание читателя и открытие файла](to-create-a-reader-and-open-a-file.md) (или [Создание синхронного средства чтения и открытие файла](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="385c2-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="385c2-115">Получите общее число выходов для файла, вызвав [**ивмреадер:: жетаутпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (или [**Ивмсинкреадер:: жетаутпуткаунт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span><span class="sxs-lookup"><span data-stu-id="385c2-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="385c2-116">Перебрать выходные данные по одному за раз, выполнив следующие действия для каждого из них:</span><span class="sxs-lookup"><span data-stu-id="385c2-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="385c2-117">Получите интерфейс [**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) для текущего вывода с помощью вызова [**Ивмреадер:: Жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (или [**ивмсинкреадер:: жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="385c2-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="385c2-118">Получите структуру [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для выходных данных, выполнив два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="385c2-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="385c2-119">Выполните первый вызов, чтобы получить размер структуры, затем выделите память для нее и передайте указатель на выделенную память во втором вызове.</span><span class="sxs-lookup"><span data-stu-id="385c2-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="385c2-120">Кроме того, можно вызвать метод [**ивммедиапропс:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), который доставляет основной тип, не требуя выделения памяти для **структуры \_ \_ типа мультимедиа WM** .</span><span class="sxs-lookup"><span data-stu-id="385c2-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="385c2-121">Можно пропустить выходные данные неправильного основного типа.</span><span class="sxs-lookup"><span data-stu-id="385c2-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="385c2-122">Получите основной тип носителя и подтип носителя из структуры **\_ \_ типа мультимедиа WM** .</span><span class="sxs-lookup"><span data-stu-id="385c2-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="385c2-123">Эти значения хранятся в элементах данных **мажортипе** и **подтип** соответственно.</span><span class="sxs-lookup"><span data-stu-id="385c2-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="385c2-124">Проверьте значение **WM \_ Media \_ Type. форматтипе**.</span><span class="sxs-lookup"><span data-stu-id="385c2-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="385c2-125">Указывает тип структуры, содержащейся в буфере, на **WM \_ Media \_ Type. пбформат**.</span><span class="sxs-lookup"><span data-stu-id="385c2-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="385c2-126">Дополнительные сведения о типах форматов см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="385c2-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="385c2-127">Выделите память для хранения структуры типа, указанного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="385c2-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="385c2-128">Скопируйте структуру в выделенную память.</span><span class="sxs-lookup"><span data-stu-id="385c2-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="385c2-129">Для аудио и видео эта структура предоставляет необходимую информацию о том, как должны подготавливаться данные.</span><span class="sxs-lookup"><span data-stu-id="385c2-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="385c2-130">Синхронное средство чтения также предоставляет методы для получения связей между выходными числами и номерами потоков.</span><span class="sxs-lookup"><span data-stu-id="385c2-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="385c2-131">Дополнительные сведения см. [в разделе Поиск номеров потоков и выходных номеров](to-find-stream-numbers-and-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="385c2-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="385c2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="385c2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="385c2-133">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="385c2-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="385c2-134">**Интерфейс Ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="385c2-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="385c2-135">**Интерфейс Ивмаутпутмедиапропс**</span><span class="sxs-lookup"><span data-stu-id="385c2-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="385c2-136">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="385c2-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="385c2-137">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="385c2-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="385c2-138">**Работа с выходами**</span><span class="sxs-lookup"><span data-stu-id="385c2-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




