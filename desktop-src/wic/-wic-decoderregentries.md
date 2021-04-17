---
description: Decoder-Specific записи реестра
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific записи реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719729"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="7a63a-103">Decoder-Specific записи реестра</span><span class="sxs-lookup"><span data-stu-id="7a63a-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="7a63a-104">В дополнение к записям реестра, необходимым для всех кодировщиков и декодеров, для декодеров требуются следующие записи реестра.</span><span class="sxs-lookup"><span data-stu-id="7a63a-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="7a63a-105">Эти записи регистрируют декодер в категории декодеров компонента обработки изображений Windows (WIC).</span><span class="sxs-lookup"><span data-stu-id="7a63a-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="7a63a-106">Первым идентификатором GUID в этих записях является идентификатор категории (CATID) для [**wicbitmapencoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="7a63a-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="7a63a-107">Как отмечалось в разделе [Обнаружение и арбитраж](-wic-howwicworks.md) , как работает компонент Windows Imaging, механизм, который позволяет обнаружить соответствующий декодер для определенного изображения во время выполнения, основан на соответствии идентифицирующему шаблону, внедренному в файл изображения, с шаблоном, указанным в записи реестра декодера.</span><span class="sxs-lookup"><span data-stu-id="7a63a-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="7a63a-108">Чтобы включить обнаружение декодеров во время выполнения, необходимо зарегистрировать уникальный идентифицирующий шаблон для формата изображения следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7a63a-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="7a63a-109">Все эти записи реестра являются обязательными, за исключением записи **EndOfStream** , которая является необязательной, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7a63a-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="7a63a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7a63a-110">Value</span></span>       | <span data-ttu-id="7a63a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7a63a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a63a-112">Положение</span><span class="sxs-lookup"><span data-stu-id="7a63a-112">Position</span></span>    | <span data-ttu-id="7a63a-113">Смещение в файле, где можно найти шаблон.</span><span class="sxs-lookup"><span data-stu-id="7a63a-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7a63a-114">Длина</span><span class="sxs-lookup"><span data-stu-id="7a63a-114">Length</span></span>      | <span data-ttu-id="7a63a-115">Длина шаблона.</span><span class="sxs-lookup"><span data-stu-id="7a63a-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7a63a-116">Модель</span><span class="sxs-lookup"><span data-stu-id="7a63a-116">Pattern</span></span>     | <span data-ttu-id="7a63a-117">Фактические биты, составляющие шаблон.</span><span class="sxs-lookup"><span data-stu-id="7a63a-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="7a63a-118">Это биты, которые сопоставляются с идентифицирующим шаблоном в файле изображения во время обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7a63a-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="7a63a-119">Mask</span><span class="sxs-lookup"><span data-stu-id="7a63a-119">Mask</span></span>        | <span data-ttu-id="7a63a-120">Позволяет использовать подстановочные значения в шаблонах.</span><span class="sxs-lookup"><span data-stu-id="7a63a-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="7a63a-121">Маска применяется путем выполнения логической операции AND над шаблоном и маской.</span><span class="sxs-lookup"><span data-stu-id="7a63a-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="7a63a-122">Любой бит в шаблоне, соответствующий биту маски со значением 0, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7a63a-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="7a63a-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="7a63a-123">EndOfStream</span></span> | <span data-ttu-id="7a63a-124">Смещение идентифицирующего шаблона должно быть вычислено с конца потока, а не с начала.</span><span class="sxs-lookup"><span data-stu-id="7a63a-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="7a63a-125">Некоторые форматы изображений помещают идентифицирующий шаблон в конец файла или рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="7a63a-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="7a63a-126">Поскольку значение по умолчанию — поиск с начала, если шаблон не находится ближе к концу файла, эту запись можно опустить.</span><span class="sxs-lookup"><span data-stu-id="7a63a-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="7a63a-127">Кодек может поддерживать более одного идентифицирующего шаблона.</span><span class="sxs-lookup"><span data-stu-id="7a63a-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="7a63a-128">В этом случае следует повторить все ключи в разделе **классы hKey root CLSID \_ \_ \\ \\ {декодер CLSID} \\** и использовать числовой ключ (0 в примере) для различения различных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7a63a-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="7a63a-129">Необходимо включить каждое из четырех значений в ключе для каждого шаблона.</span><span class="sxs-lookup"><span data-stu-id="7a63a-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="7a63a-130">Регистрация формата контейнера с помощью средств чтения метаданных</span><span class="sxs-lookup"><span data-stu-id="7a63a-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="7a63a-131">При создании нового формата контейнера для кодека необходимо также создать записи реестра для поддержки обнаружения модулей чтения метаданных для блоков метаданных в изображениях так же, как и для модулей записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="7a63a-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="7a63a-132">Следующие записи должны быть созданы с идентификатором класса (CLSID) модуля чтения метаданных для каждого формата метаданных, поддерживаемого вашим форматом контейнера.</span><span class="sxs-lookup"><span data-stu-id="7a63a-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="7a63a-133">(Обратите внимание, что если кодек использует контейнер формата TIFF, эта информация уже находится в реестре.)</span><span class="sxs-lookup"><span data-stu-id="7a63a-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="7a63a-134">Так как записи для модулей чтения метаданных также используются для обнаружения, они очень похожи на записи для декодеров.</span><span class="sxs-lookup"><span data-stu-id="7a63a-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="7a63a-135">Эти записи используются фабрикой компонентов для поиска модулей чтения метаданных, поддерживаемых контейнером, и выбора соответствующего элемента, когда реализация [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) запрашивает средство чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="7a63a-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="7a63a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7a63a-136">Value</span></span>      | <span data-ttu-id="7a63a-137">Описание</span><span class="sxs-lookup"><span data-stu-id="7a63a-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a63a-138">Положение</span><span class="sxs-lookup"><span data-stu-id="7a63a-138">Position</span></span>   | <span data-ttu-id="7a63a-139">Смещение в контейнере блока метаданных, в котором можно найти заголовок метаданных.</span><span class="sxs-lookup"><span data-stu-id="7a63a-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="7a63a-140">Для блоков метаданных верхнего уровня это смещение в файловом потоке.</span><span class="sxs-lookup"><span data-stu-id="7a63a-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="7a63a-141">Для блоков метаданных, вложенных в другие блоки метаданных, это смещение относительно содержащего его блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="7a63a-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="7a63a-142">Модель</span><span class="sxs-lookup"><span data-stu-id="7a63a-142">Pattern</span></span>    | <span data-ttu-id="7a63a-143">Фактические биты, составляющие шаблон.</span><span class="sxs-lookup"><span data-stu-id="7a63a-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="7a63a-144">Это биты, которые сопоставляются с идентифицирующим шаблоном в файле изображения во время обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7a63a-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="7a63a-145">Mask</span><span class="sxs-lookup"><span data-stu-id="7a63a-145">Mask</span></span>       | <span data-ttu-id="7a63a-146">Заголовок метаданных обычно определяется обработчиком метаданных.</span><span class="sxs-lookup"><span data-stu-id="7a63a-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="7a63a-147">Следует использовать стандартный заголовок метаданных для каждого модуля чтения, если по какой-либо причине шаблон должен иметь другой формат в вашем контейнере.</span><span class="sxs-lookup"><span data-stu-id="7a63a-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="7a63a-148">Смещение в виде значения</span><span class="sxs-lookup"><span data-stu-id="7a63a-148">DataOffset</span></span> | <span data-ttu-id="7a63a-149">Смещение от начала заголовка метаданных, с которого начинаются фактические данные.</span><span class="sxs-lookup"><span data-stu-id="7a63a-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="7a63a-150">В случаях, когда метаданные расположены не в указанном смещении от заголовка, эту запись можно опустить.</span><span class="sxs-lookup"><span data-stu-id="7a63a-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="7a63a-151">См. также</span><span class="sxs-lookup"><span data-stu-id="7a63a-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7a63a-152">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7a63a-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7a63a-153">Записи реестра, относящиеся к кодировщику</span><span class="sxs-lookup"><span data-stu-id="7a63a-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="7a63a-154">Интеграция с Фотоальбомом Windows и проводником Windows</span><span class="sxs-lookup"><span data-stu-id="7a63a-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="7a63a-155">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="7a63a-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="7a63a-156">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="7a63a-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



