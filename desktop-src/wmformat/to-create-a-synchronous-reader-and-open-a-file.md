---
title: Создание синхронного средства чтения и открытие файла
description: Создание синхронного средства чтения и открытие файла
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Расширенный системный формат (ASF), создание читателей
- ASF (Расширенный системный формат), создание читателей
- Расширенный формат систем (ASF), открытие файлов
- ASF (Расширенный системный формат), открытие файлов
- синхронные читатели, создание
- синхронные читатели, открытие файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700823"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="a6ba8-109">Создание синхронного средства чтения и открытие файла</span><span class="sxs-lookup"><span data-stu-id="a6ba8-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="a6ba8-110">Прежде чем выполнять какие-либо действия с синхронным модулем чтения, необходимо создать синхронный объект Reader и загрузить файл для чтения.</span><span class="sxs-lookup"><span data-stu-id="a6ba8-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="a6ba8-111">Чтобы инициализировать синхронное средство чтения и открыть файл, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a6ba8-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="a6ba8-112">Создайте синхронный объект Reader, вызвав функцию [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .</span><span class="sxs-lookup"><span data-stu-id="a6ba8-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="a6ba8-113">Необходимо указать требуемый уровень Rights Management для нового объекта модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="a6ba8-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="a6ba8-114">Доступные режимы перечислены в типе перечисления **\_ Rights ВМТ** .</span><span class="sxs-lookup"><span data-stu-id="a6ba8-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="a6ba8-115">Укажите файл для чтения путем вызова [**ивмсинкреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span><span class="sxs-lookup"><span data-stu-id="a6ba8-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="a6ba8-116">Синхронное средство чтения также поддерживает использование интерфейса **IStream** com для открытия файлов.</span><span class="sxs-lookup"><span data-stu-id="a6ba8-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="a6ba8-117">Интерфейс **IStream** можно реализовать любым выбранным способом.</span><span class="sxs-lookup"><span data-stu-id="a6ba8-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="a6ba8-118">После открытия требуемого файла в **IStream** можно выполнить приведенные выше действия, за исключением того, что необходимо вызвать [**Ивмсинкреадер:: опенстреам**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) вместо **ивмсинкреадер:: Open** на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="a6ba8-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6ba8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a6ba8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6ba8-120">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="a6ba8-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="a6ba8-121">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="a6ba8-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




