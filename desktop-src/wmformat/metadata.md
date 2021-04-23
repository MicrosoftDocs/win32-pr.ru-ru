---
title: Метаданные
description: Метаданные для целей этого пакета SDK — это сведения, описывающие ASF-файл или содержимое файла.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK, общие сведения о метаданных
- Улучшенный системный формат (ASF), общие сведения о метаданных
- ASF (Расширенный системный формат), общие сведения о метаданных
- метаданные, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332296"
---
# <a name="metadata"></a><span data-ttu-id="51138-107">Метаданные</span><span class="sxs-lookup"><span data-stu-id="51138-107">Metadata</span></span>

<span data-ttu-id="51138-108">Метаданные для целей этого пакета SDK — это сведения, описывающие ASF-файл или содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="51138-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="51138-109">Раздел заголовка файла ASF содержит все метаданные, связанные с этим файлом.</span><span class="sxs-lookup"><span data-stu-id="51138-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="51138-110">Отдельные элементы метаданных в файле ASF называются атрибутами.</span><span class="sxs-lookup"><span data-stu-id="51138-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="51138-111">У каждого атрибута есть имя и значение.</span><span class="sxs-lookup"><span data-stu-id="51138-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="51138-112">В этой документации глобальные константы используются для обнаружения атрибутов.</span><span class="sxs-lookup"><span data-stu-id="51138-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="51138-113">Например, заголовок ASF-файла хранится в атрибуте **g \_ всзвмтитле** .</span><span class="sxs-lookup"><span data-stu-id="51138-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="51138-114">Некоторые атрибуты определяются в пакете SDK формата Windows Media для решения наиболее распространенных потребностей метаданных.</span><span class="sxs-lookup"><span data-stu-id="51138-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="51138-115">Кроме того, можно создавать собственные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="51138-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="51138-116">Однако следует соблюдать осторожность при именовании настраиваемых атрибутов, так как другие разработчики приложений могут использовать одни и те же имена, и конфликты могут возникать.</span><span class="sxs-lookup"><span data-stu-id="51138-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="51138-117">Некоторые атрибуты задаются пакетом SDK и не могут быть изменены вручную.</span><span class="sxs-lookup"><span data-stu-id="51138-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="51138-118">Например, при индексировании файла ASF пакет SDK устанавливает атрибут **g \_ всзвмсикабле** , чтобы увидеть, что теперь файл можно считать из любой заданной точки.</span><span class="sxs-lookup"><span data-stu-id="51138-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="51138-119">Другие атрибуты являются исключительно информационными и должны быть заданы вручную.</span><span class="sxs-lookup"><span data-stu-id="51138-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="51138-120">Например, если вы хотите отследить автора файла, следует установить параметр **g \_ всзвмаусор**.</span><span class="sxs-lookup"><span data-stu-id="51138-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="51138-121">Пакет SDK для формата Windows Media обеспечивает поддержку атрибутов, применяемых ко всему файлу, и атрибутов, которые применяются к отдельным потокам.</span><span class="sxs-lookup"><span data-stu-id="51138-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="51138-122">Для редактирования метаданных в MP3-файлах можно использовать пакет SDK Windows Media Format, хотя для обеспечения совместимости с другими программами обработки MP3 следует всегда использовать совместимые с ID3 атрибуты в файлах MP3.</span><span class="sxs-lookup"><span data-stu-id="51138-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51138-123">См. также</span><span class="sxs-lookup"><span data-stu-id="51138-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51138-124">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="51138-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="51138-125">**Объект редактора метаданных**</span><span class="sxs-lookup"><span data-stu-id="51138-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="51138-126">**Компоненты метаданных**</span><span class="sxs-lookup"><span data-stu-id="51138-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="51138-127">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="51138-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




