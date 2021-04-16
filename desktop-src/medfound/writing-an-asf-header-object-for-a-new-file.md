---
description: Запись объекта заголовка ASF для нового файла
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Запись объекта заголовка ASF для нового файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702918"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="c1a69-103">Запись объекта заголовка ASF для нового файла</span><span class="sxs-lookup"><span data-stu-id="c1a69-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="c1a69-104">Объект ASF Контентинфо сохраняет сведения об объекте заголовка ASF для файла.</span><span class="sxs-lookup"><span data-stu-id="c1a69-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="c1a69-105">При создании или изменении ASF-файла необходимо создать объект заголовка.</span><span class="sxs-lookup"><span data-stu-id="c1a69-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="c1a69-106">Для этого приложение должно предоставить профиль кодирования содержимого объекту Контентинфо, чтобы он знал о характеристиках создаваемого файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c1a69-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="c1a69-107">Для записи нового файла можно использовать объект Контентинфо для:</span><span class="sxs-lookup"><span data-stu-id="c1a69-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="c1a69-108">Собирайте данные заголовка из объекта профиля создаваемого файла,</span><span class="sxs-lookup"><span data-stu-id="c1a69-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="c1a69-109">Заполните различные объекты заголовков в библиотеке ASF, которые поддерживаются внутренне Media Foundation,</span><span class="sxs-lookup"><span data-stu-id="c1a69-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="c1a69-110">Инициализируйте [мультиплексор ASF](asf-multiplexer.md) для создания пакета данных ASF и</span><span class="sxs-lookup"><span data-stu-id="c1a69-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="c1a69-111">Создайте объект верхнего уровня заголовка в двоичном формате, который может быть записан в файл.</span><span class="sxs-lookup"><span data-stu-id="c1a69-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="c1a69-112">Дополнительные сведения о профилях см. в разделе [профиль ASF](asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="c1a69-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="c1a69-113">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="c1a69-113">This section contains the following topics:</span></span>



| <span data-ttu-id="c1a69-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="c1a69-114">Topic</span></span>                                                                                                              | <span data-ttu-id="c1a69-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c1a69-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1a69-116">Инициализация объекта Контентинфо нового ASF-файла</span><span class="sxs-lookup"><span data-stu-id="c1a69-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="c1a69-117">Описывает метод [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , который инициализирует объект контентинфо со сведениями о заголовке, хранящимися в объекте Profile.</span><span class="sxs-lookup"><span data-stu-id="c1a69-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="c1a69-118">Задание свойств в объекте Контентинфо</span><span class="sxs-lookup"><span data-stu-id="c1a69-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="c1a69-119">Сведения о различных свойствах конфигурации, которые должны быть установлены для объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="c1a69-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="c1a69-120">Создание нового объекта заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="c1a69-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="c1a69-121">Создание буфера мультимедиа, содержащего фактический объект заголовка ASF нового файла, из объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="c1a69-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="c1a69-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c1a69-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1a69-123">Объект Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="c1a69-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="c1a69-124">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="c1a69-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="c1a69-125">Структура файла ASF</span><span class="sxs-lookup"><span data-stu-id="c1a69-125">ASF File Structure</span></span>
</dt> </dl>

 

 



