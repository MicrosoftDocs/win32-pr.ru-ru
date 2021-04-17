---
description: Объект Контентинфо ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Объект Контентинфо ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692093"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="d2f89-103">Объект Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="d2f89-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="d2f89-104">Объект ASF *контентинфо* сохраняет информацию из объекта заголовка ASF файла.</span><span class="sxs-lookup"><span data-stu-id="d2f89-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="d2f89-105">Приложение может использовать объект Контентинфо в следующих целях:</span><span class="sxs-lookup"><span data-stu-id="d2f89-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="d2f89-106">Считывает объект заголовка для существующего файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d2f89-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="d2f89-107">В этом случае объект Контентинфо анализирует объект заголовка и сохраняет сведения о файле характеристик.</span><span class="sxs-lookup"><span data-stu-id="d2f89-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="d2f89-108">Media Foundation предоставляет некоторые из этих свойств через атрибуты и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="d2f89-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="d2f89-109">Они описаны в разделе [атрибуты Media Foundation для объектов заголовка ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2f89-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="d2f89-110">Запись данных заголовка и создание объекта заголовка для нового файла.</span><span class="sxs-lookup"><span data-stu-id="d2f89-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="d2f89-111">При чтении или записи файла мультимедиа инициализируйте другие объекты ASF, такие как [Разделитель ASF](asf-splitter.md), [мультиплексор ASF](asf-multiplexer.md)и индексатор ASF.</span><span class="sxs-lookup"><span data-stu-id="d2f89-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="d2f89-112">Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d2f89-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="d2f89-113">Создание объекта Контентинфо</span><span class="sxs-lookup"><span data-stu-id="d2f89-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="d2f89-114">Чтобы создать новый экземпляр объекта Контентинфо, вызовите функцию [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="d2f89-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="d2f89-115">Этот метод возвращает указатель на пустой объект Контентинфо, который должен быть инициализирован для работы с определенным файлом ASF.</span><span class="sxs-lookup"><span data-stu-id="d2f89-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="d2f89-116">В зависимости от того, считывает ли приложение существующий файл или записывает новый ASF-файл, он должен вызвать [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) или [**Имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) для заполнения пустого объекта.</span><span class="sxs-lookup"><span data-stu-id="d2f89-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="d2f89-117">Дополнительные сведения об этих вызовах методов см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="d2f89-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="d2f89-118">Чтение объекта заголовка ASF существующего файла</span><span class="sxs-lookup"><span data-stu-id="d2f89-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="d2f89-119">Получение сведений из объектов заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="d2f89-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="d2f89-120">Запись объекта заголовка ASF для нового файла</span><span class="sxs-lookup"><span data-stu-id="d2f89-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="d2f89-121">Атрибуты Media Foundation для объектов заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="d2f89-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="d2f89-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d2f89-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f89-123">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="d2f89-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



