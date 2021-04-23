---
title: О процессе преобразования
description: О процессе преобразования
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Проигрыватель Windows Media, процесс преобразования
- Подключаемые модули проигрывателя Windows Media, преобразование
- подключаемые модули, преобразование
- подключаемые модули преобразования, процесс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069585"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="6852c-107">О процессе преобразования</span><span class="sxs-lookup"><span data-stu-id="6852c-107">About the Conversion Process</span></span>

<span data-ttu-id="6852c-108">После того как проигрыватель Windows Media создаст экземпляр подключаемого модуля преобразования, процесс продолжится следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6852c-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="6852c-109">Проигрыватель вызывает [ивмпконверт:: конвертфиле](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span><span class="sxs-lookup"><span data-stu-id="6852c-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="6852c-110">Подключаемый модуль преобразует файл, указанный в параметре *бстринпутфиле* , в формат ASF.</span><span class="sxs-lookup"><span data-stu-id="6852c-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="6852c-111">Если по какой-то причине преобразование завершается неудачей, подключаемый модуль возвращает соответствующий код ошибки, и процесс останавливается.</span><span class="sxs-lookup"><span data-stu-id="6852c-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="6852c-112">Если преобразование выполнено, подключаемый модуль помещает преобразованный файл в папку, указанную в параметре *бстрдестинатионфолдер* , и возвращает полный путь к преобразованному файлу с помощью параметра *пбстраутпутфиле* .</span><span class="sxs-lookup"><span data-stu-id="6852c-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="6852c-113">Подключаемый модуль возвращает код успешного выполнения из **конвертфиле**.</span><span class="sxs-lookup"><span data-stu-id="6852c-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="6852c-114">Проигрыватель копирует преобразованный файл в папку в иерархии папок музыки пользователя.</span><span class="sxs-lookup"><span data-stu-id="6852c-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="6852c-115">Именно там, где проигрыватель копирует файл, зависит от содержимого.</span><span class="sxs-lookup"><span data-stu-id="6852c-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="6852c-116">В рамках этого процесса проигрыватель может переименовать файл.</span><span class="sxs-lookup"><span data-stu-id="6852c-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="6852c-117">Проигрыватель копирует исходный (непреобразованный) файл в папку в иерархии папок музыки пользователя.</span><span class="sxs-lookup"><span data-stu-id="6852c-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="6852c-118">В рамках этого процесса проигрыватель может переименовать файл.</span><span class="sxs-lookup"><span data-stu-id="6852c-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="6852c-119">Это копия файла, используемая проигрывателем при синхронизации пользователем содержимого с компьютера с устройством, для которого требуется исходный формат файла.</span><span class="sxs-lookup"><span data-stu-id="6852c-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="6852c-120">Этот файл называется *теневым файлом*.</span><span class="sxs-lookup"><span data-stu-id="6852c-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="6852c-121">Проигрыватель добавляет сведения о преобразованном файле в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="6852c-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="6852c-122">Сюда входит установка значения атрибута **шадовфилепас** в новое расположение, в котором сохранен файл тени.</span><span class="sxs-lookup"><span data-stu-id="6852c-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="6852c-123">Если необходимо работать с преобразованным файлом, можно запросить библиотеку для получения содержимого с помощью атрибутов **контентдистрибутор** и **WM/уникуефилеидентифиер** .</span><span class="sxs-lookup"><span data-stu-id="6852c-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="6852c-124">Если необходимо работать с теневым файлом, необходимо извлечь объект **мультимедиа** для преобразованного файла, а затем запросить атрибут **шадовфилепас** .</span><span class="sxs-lookup"><span data-stu-id="6852c-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="6852c-125">См. раздел [Добавление метаданных в преобразованные файлы](adding-metadata-to-converted-files.md).</span><span class="sxs-lookup"><span data-stu-id="6852c-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6852c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6852c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6852c-127">**О подключаемых модулях преобразования**</span><span class="sxs-lookup"><span data-stu-id="6852c-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="6852c-128">**Добавление метаданных в преобразованные файлы**</span><span class="sxs-lookup"><span data-stu-id="6852c-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="6852c-129">**Считывание значений атрибутов**</span><span class="sxs-lookup"><span data-stu-id="6852c-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="6852c-130">**Атрибут Шадовфилепас**</span><span class="sxs-lookup"><span data-stu-id="6852c-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="6852c-131">**Атрибут WM/Контентдистрибутор**</span><span class="sxs-lookup"><span data-stu-id="6852c-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="6852c-132">**Атрибут WM/Уникуефилеидентифиер**</span><span class="sxs-lookup"><span data-stu-id="6852c-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




