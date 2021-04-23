---
title: Создание средства чтения и открытие файла
description: Создание средства чтения и открытие файла
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Расширенный системный формат (ASF), создание читателей
- ASF (Расширенный системный формат), создание читателей
- Расширенный формат систем (ASF), открытие файлов
- ASF (Расширенный системный формат), открытие файлов
- асинхронные читатели, создание
- асинхронные читатели, открытие файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789216"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="b8e5c-109">Создание средства чтения и открытие файла</span><span class="sxs-lookup"><span data-stu-id="b8e5c-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="b8e5c-110">Прежде чем выполнять какие-либо действия с модулем чтения, необходимо создать объект Reader и загрузить файл для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="b8e5c-111">Чтобы инициализировать средство чтения и открыть файл, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="b8e5c-112">Создайте объект Reader, вызвав функцию [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) .</span><span class="sxs-lookup"><span data-stu-id="b8e5c-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="b8e5c-113">Необходимо указать требуемый уровень Rights Management для нового объекта модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="b8e5c-114">Доступные режимы перечислены в типе перечисления [**\_ Rights ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="b8e5c-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="b8e5c-115">Укажите файл для чтения путем вызова [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span><span class="sxs-lookup"><span data-stu-id="b8e5c-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="b8e5c-116">Необходимо указать интерфейс обратного вызова модуля чтения, который будет использоваться средством чтения.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="b8e5c-117">Дополнительные сведения о обратном вызове модуля чтения см. в разделе [Реализация сообщений модуля чтения в обратном вызове OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="b8e5c-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="b8e5c-118">Дождитесь открытия файла средством чтения.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="b8e5c-119">При вызове метода **Open** для загрузки файла он сразу же возвращается и возобновляет обработку в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="b8e5c-120">Дождитесь завершения операций, получив событие, когда обратный вызов **OnStatus** получает \_ сообщение о состоянии ВМТ Opened.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="b8e5c-121">Модуль чтения также поддерживает использование интерфейса **IStream** com для открытия файлов.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="b8e5c-122">Интерфейс **IStream** можно реализовать любым выбранным способом.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="b8e5c-123">После открытия требуемого файла в **IStream** можно выполнить приведенные выше действия, за исключением того, что необходимо вызвать [**IWMReaderAdvanced2:: опенстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) вместо **ивмреадер:: Open** на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="b8e5c-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8e5c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b8e5c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e5c-125">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="b8e5c-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="b8e5c-126">**Интерфейс IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="b8e5c-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="b8e5c-127">**Интерфейс Ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b8e5c-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="b8e5c-128">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="b8e5c-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b8e5c-129">**Использование методов обратного вызова**</span><span class="sxs-lookup"><span data-stu-id="b8e5c-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




