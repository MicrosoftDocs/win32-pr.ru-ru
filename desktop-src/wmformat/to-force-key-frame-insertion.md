---
title: Принудительная Вставка Key-Frame
description: Принудительная Вставка Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Расширенный системный формат (ASF), принудительная вставка ключевых кадров
- ASF (Расширенный системный формат), принудительная вставка ключевых кадров
- Расширенный формат систем (ASF), вставка ключевых кадров
- ASF (Расширенный системный формат), вставка ключевых кадров
- ключевые кадры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104487357"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="81bee-108">Принудительная Вставка Key-Frame</span><span class="sxs-lookup"><span data-stu-id="81bee-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="81bee-109">Кодек Windows Media Video 9 поддерживает принудительную вставку по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="81bee-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="81bee-110">При передаче образца в модуль записи можно указать, что он должен быть закодирован в виде [*ключевого кадра*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="81bee-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="81bee-111">Чтобы принудительно вставить ключевые кадры для примера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="81bee-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="81bee-112">Выделите буфер для хранения образца и получите указатель на интерфейс [**инссбуффер**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) , содержащий буфер, вызвав [**Ивмвритер:: аллокатесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="81bee-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="81bee-113">Извлеките расположение и размер буфера, созданного на шаге 1, вызвав [**инссбуффер:: жетбуфферандленгс**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span><span class="sxs-lookup"><span data-stu-id="81bee-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="81bee-114">Скопируйте образец данных в буферное расположение, убедившись, что переданный образец будет помещаться в выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="81bee-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="81bee-115">В зависимости от источника выборки можно использовать различные функции для копирования данных.</span><span class="sxs-lookup"><span data-stu-id="81bee-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="81bee-116">Например, при копировании потока из AVI-файла можно использовать функцию AVI **авистреамреад**.</span><span class="sxs-lookup"><span data-stu-id="81bee-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="81bee-117">Обновите объем данных, используемых в буфере, чтобы отразить фактический размер образца путем вызова [**инссбуффер:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="81bee-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="81bee-118">Получите указатель на интерфейс [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) , вызвав **Инссбуффер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="81bee-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="81bee-119">Задайте пример в качестве принудительного ключевого кадра, вызвав метод [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) , чтобы установить \_ свойство WM сампликстенсионгуид \_ аутпутклеанпоинт.</span><span class="sxs-lookup"><span data-stu-id="81bee-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="81bee-120">Это свойство имеет логическое значение. Задайте для него **значение true**.</span><span class="sxs-lookup"><span data-stu-id="81bee-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="81bee-121">Передайте интерфейс буфера записи, а также входной номер и время выборки с помощью метода [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="81bee-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81bee-122">См. также</span><span class="sxs-lookup"><span data-stu-id="81bee-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81bee-123">**Ивмвритер:: Вритесампле**</span><span class="sxs-lookup"><span data-stu-id="81bee-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="81bee-124">**Написание образцов**</span><span class="sxs-lookup"><span data-stu-id="81bee-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="81bee-125">**Кодирование переменной скорости (VBR)**</span><span class="sxs-lookup"><span data-stu-id="81bee-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="81bee-126">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="81bee-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




