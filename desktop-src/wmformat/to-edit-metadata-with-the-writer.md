---
title: Изменение метаданных с помощью модуля записи
description: Изменение метаданных с помощью модуля записи
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK, Редактирование метаданных с помощью модуля записи
- Пакет SDK для Windows Media Format, Редактирование метаданных
- Расширенный системный формат (ASF), Редактирование метаданных с помощью модуля записи
- ASF (Расширенный системный формат), Редактирование метаданных с помощью модуля записи
- Расширенный системный формат (ASF), Редактирование метаданных
- ASF (Расширенный системный формат), Редактирование метаданных
- метаданные, редактирование с помощью модуля записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412703"
---
# <a name="to-edit-metadata-with-the-writer"></a><span data-ttu-id="00e9f-110">Изменение метаданных с помощью модуля записи</span><span class="sxs-lookup"><span data-stu-id="00e9f-110">To Edit Metadata with the Writer</span></span>

<span data-ttu-id="00e9f-111">Вы можете обращаться непосредственно к модулю записи, а также к метаданным, которые будут переключаться в заголовок файла.</span><span class="sxs-lookup"><span data-stu-id="00e9f-111">You can access, directly from the writer, the metadata that will go into the header of the file.</span></span> <span data-ttu-id="00e9f-112">Вызовите метод **QueryInterface** любого интерфейса в объекте модуля записи, чтобы получить указатель на интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) или [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="00e9f-112">Call the **QueryInterface** method of any interface in the writer object to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interface.</span></span> <span data-ttu-id="00e9f-113">После создания указателя на соответствующий интерфейс можно манипулировать метаданными точно так же, как при загрузке файла в объект редактора метаданных.</span><span class="sxs-lookup"><span data-stu-id="00e9f-113">After you have a pointer to the appropriate interface, you can manipulate the metadata just as you would if you had loaded the file in the metadata editor object.</span></span> <span data-ttu-id="00e9f-114">Дополнительные сведения об изменении метаданных см. [в разделе Работа с метаданными](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="00e9f-114">For more information about editing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

<span data-ttu-id="00e9f-115">Перед вызовом [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)необходимо внести все изменения в метаданные.</span><span class="sxs-lookup"><span data-stu-id="00e9f-115">You must make all changes to the metadata before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

> [!Note]  
> <span data-ttu-id="00e9f-116">Если задать метаданные для файла, записать файл, а затем подготовиться к записи нового файла без освобождения модуля записи, то некоторые метаданные, заданные для первого файла, останутся установленными и будут включаться в последующие файлы.</span><span class="sxs-lookup"><span data-stu-id="00e9f-116">If you set metadata for a file, write the file, and then prepare to write a new file without releasing the writer, some metadata that was set for the first file will remain set and will be included with subsequent files.</span></span> <span data-ttu-id="00e9f-117">При записи нескольких файлов с одним и тем же экземпляром объекта модуля записи у вас есть два варианта: проверять все метаданные перед записью каждого файла или записывать только метаданные модуля записи, которые применяются ко всем записываемым файлам.</span><span class="sxs-lookup"><span data-stu-id="00e9f-117">When writing several files with the same instance of the writer object, you have two options: check all the metadata before writing each file, or only write in the writer metadata that applies to all of the files you are writing.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="00e9f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="00e9f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e9f-119">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="00e9f-119">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




