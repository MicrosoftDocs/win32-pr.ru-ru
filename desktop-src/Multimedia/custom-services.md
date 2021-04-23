---
title: Настраиваемые службы
description: Настраиваемые службы
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- Ввод-вывод файлов мультимедиа, пользовательские службы
- Ввод-вывод файлов, пользовательские службы
- входные и выходные данные (ввод-вывод), пользовательские службы
- Ввод-вывод (входные и выходные данные), пользовательские службы
- пользовательский ввод-вывод
- Функция Ммиоинсталлиопрок
- Функция Ммиупен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069957"
---
# <a name="custom-services"></a><span data-ttu-id="22c4c-110">Настраиваемые службы</span><span class="sxs-lookup"><span data-stu-id="22c4c-110">Custom Services</span></span>

<span data-ttu-id="22c4c-111">Службы файлового ввода-вывода используют процедуры ввода-вывода для обработки физических входных и выходных данных, связанных с чтением и записью в различные типы систем хранения, таких как архивные системы и системы хранения баз данных.</span><span class="sxs-lookup"><span data-stu-id="22c4c-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="22c4c-112">Предопределенные процедуры ввода-вывода существуют для стандартных файловых систем и для файлов памяти, но можно предоставить пользовательскую процедуру ввода-вывода для доступа к уникальной системе хранения с помощью функции [**ммиоинсталлиопрок**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .</span><span class="sxs-lookup"><span data-stu-id="22c4c-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="22c4c-113">Чтобы открыть файл с помощью пользовательской процедуры ввода-вывода, используйте функцию [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="22c4c-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="22c4c-114">Включите знак плюс (+) или константу КФСЕПЧАР в имя файла, чтобы отделить имя физического файла от имени элемента файла, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="22c4c-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="22c4c-115">В следующем примере открывается элемент File с именем "Element" из файла с именем FILENAME. ДУГИ</span><span class="sxs-lookup"><span data-stu-id="22c4c-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="22c4c-116">Когда диспетчер файлового ввода-вывода встречает знак плюс в имени файла, он проверяет расширение имени файла, чтобы определить, какую процедуру ввода-вывода следует связать с файлом.</span><span class="sxs-lookup"><span data-stu-id="22c4c-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="22c4c-117">В предыдущем примере диспетчер файлового ввода-вывода попытается использовать процедуру ввода-вывода, связанную с. Расширение имени файла ARC; Эта процедура ввода-вывода была бы установлена с помощью [**ммиоинсталлиопрок**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span><span class="sxs-lookup"><span data-stu-id="22c4c-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="22c4c-118">Если процедура ввода-вывода не установлена, [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="22c4c-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="22c4c-119">Процедуры ввода-вывода должны отвечать на следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="22c4c-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="22c4c-120">**ММИОМ \_ Закрыть**</span><span class="sxs-lookup"><span data-stu-id="22c4c-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="22c4c-121">**ММИОМ \_ Открыть**</span><span class="sxs-lookup"><span data-stu-id="22c4c-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="22c4c-122">**ММИОМ \_ чтение**</span><span class="sxs-lookup"><span data-stu-id="22c4c-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="22c4c-123">**ММИОМ \_ запись**</span><span class="sxs-lookup"><span data-stu-id="22c4c-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="22c4c-124">**ММИОМ \_ Поиск**</span><span class="sxs-lookup"><span data-stu-id="22c4c-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="22c4c-125">**\_Переименование ммиом**</span><span class="sxs-lookup"><span data-stu-id="22c4c-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="22c4c-126">**ММИОМ \_ вритефлуш**</span><span class="sxs-lookup"><span data-stu-id="22c4c-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="22c4c-127">Вы также можете создавать пользовательские сообщения и передавать их в процедуру ввода-вывода с помощью функции [**ммиосендмессаже**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) .</span><span class="sxs-lookup"><span data-stu-id="22c4c-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="22c4c-128">Если вы определяете собственные сообщения, убедитесь, что они определены на уровне или выше значения, определенного \_ константой пользователя ммиом.</span><span class="sxs-lookup"><span data-stu-id="22c4c-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="22c4c-129">В дополнение к обработке сообщений процедура ввода-вывода должна поддерживать элемент **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) (на который указывает параметр *лпммиоинфо* функции **ммиупен** ).</span><span class="sxs-lookup"><span data-stu-id="22c4c-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="22c4c-130">Элемент **лдискоффсет** всегда должен содержать смещение файла в расположении, \_ к которому будет обращаться следующий ммиом для чтения или ммиом \_ сообщения.</span><span class="sxs-lookup"><span data-stu-id="22c4c-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="22c4c-131">Смещение указывается в байтах и задается относительно начала файла.</span><span class="sxs-lookup"><span data-stu-id="22c4c-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="22c4c-132">Процедура ввода-вывода может использовать элемент **адвинфо** для сохранения необходимой информации о состоянии.</span><span class="sxs-lookup"><span data-stu-id="22c4c-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="22c4c-133">Процедура ввода-вывода не должна изменять никакие другие члены структуры **ммиоинфо** .</span><span class="sxs-lookup"><span data-stu-id="22c4c-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 