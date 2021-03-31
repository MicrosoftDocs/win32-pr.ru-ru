---
title: О файлах SAMI
description: О файлах SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель проигрывателя Windows Media, синхронизированный доступный обмен мультимедийными данными (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media Mobile, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX, синхронизированный доступный медиа-обмен (SAMI)
- Синхронизированный доступный мультимедийный обмен (SAMI), файлы
- SAMI (синхронизированный доступный медиа-обмен), файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888503"
---
# <a name="about-sami-files"></a><span data-ttu-id="f3c0b-112">О файлах SAMI</span><span class="sxs-lookup"><span data-stu-id="f3c0b-112">About SAMI Files</span></span>

<span data-ttu-id="f3c0b-113">Файлы SAMI — это текстовые файлы, имеющие расширение имени файла. SMI или Sami.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-113">SAMI files are text files that have an .smi or .sami file name extension.</span></span> <span data-ttu-id="f3c0b-114">Они содержат текстовые строки, используемые для синхронизированных закрытых субтитров, субтитров и звуковых описаний.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-114">They contain the text strings used for synchronized closed captions, subtitles, and audio descriptions.</span></span> <span data-ttu-id="f3c0b-115">Они также указывают параметры времени, используемые элементом управления проигрывателем Windows Media для синхронизации текста субтитров с аудио или видео содержимым.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-115">They also specify the timing parameters used by the Windows Media Player control to synchronize closed caption text with audio or video content.</span></span> <span data-ttu-id="f3c0b-116">Когда файл цифрового носителя достигает времени, указанного в файле SAMI, текст изменяется соответствующим образом в области Отображение скрытых субтитров на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-116">When a digital media file reaches a time designated in the SAMI file, the text changes accordingly in the closed caption display area of the webpage.</span></span>

<span data-ttu-id="f3c0b-117">Для создания файла SAMI не требуется специальное программное обеспечение, отличное от простого текстового редактора (например, Microsoft Notepad).</span><span class="sxs-lookup"><span data-stu-id="f3c0b-117">Other than a simple text editor (such as Microsoft Notepad), special software is not required to create a SAMI file.</span></span> <span data-ttu-id="f3c0b-118">SAMId и HTML общие элементы, такие как <HEAD> теги и <BODY> .</span><span class="sxs-lookup"><span data-stu-id="f3c0b-118">SAMI and HTML share common elements, such as the <HEAD> and <BODY> tags.</span></span> <span data-ttu-id="f3c0b-119">Как и в HTML, теги, используемые в файлах SAMId, должны всегда использоваться в парах.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-119">As in HTML, tags used in SAMI files must always be used in pairs.</span></span> <span data-ttu-id="f3c0b-120">Например, элемент BODY начинается с <BODY> тега и всегда должен заканчиваться </BODY> тегом.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-120">For example, a BODY element begins with a <BODY> tag and must always end with a </BODY> tag.</span></span>

<span data-ttu-id="f3c0b-121">Для основного файла SAMI требуются три фундаментальных тега: <SAMI> , <HEAD> и <BODY> .</span><span class="sxs-lookup"><span data-stu-id="f3c0b-121">A basic SAMI file requires three fundamental tags: <SAMI>, <HEAD>, and <BODY>.</span></span>

<span data-ttu-id="f3c0b-122"><SAMI>Тег определяет документ как samid, чтобы другие приложения могли распознать свой формат файла.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-122">The <SAMI> tag identifies the document as a SAMI document so other applications can recognize its file format.</span></span>

<span data-ttu-id="f3c0b-123">Между тегами <HEAD> и </HEAD> вы определяете основные рекомендации и другие сведения о форматировании для samiского документа, такие как заголовок документа, общие сведения и свойства стиля для скрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-123">Between the <HEAD> and </HEAD> tags, you define basic guidelines and other format information for the SAMI document, such as the document title, general information, and style properties for closed captions.</span></span> <span data-ttu-id="f3c0b-124">Как и HTML, содержимое, объявленное в ГОЛОВном элементе, не отображается в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-124">Like HTML, content declared within the HEAD element does not display as output.</span></span>

<span data-ttu-id="f3c0b-125">Элементы и атрибуты, определенные между тегами <BODY> и </BODY> , отображают содержимое, видимое пользователю.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-125">Elements and attributes defined between the <BODY> and </BODY> tags display content seen by the user.</span></span> <span data-ttu-id="f3c0b-126">В SAMId элемент BODY содержит параметры для синхронизации и текстовые строки, используемые для закрытых заголовков.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-126">In SAMI, the BODY element contains the parameters for synchronization and the text strings used for closed captions.</span></span>

<span data-ttu-id="f3c0b-127">Элемент STYLE, определенный в ГОЛОВном элементе, предоставляет дополнительные возможности в SAMI.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-127">Defined within the HEAD element, the STYLE element provides for added functionality in SAMI.</span></span> <span data-ttu-id="f3c0b-128">Между тегами <STYLE> и </STYLE> можно определить несколько селекторов каскадных таблиц стилей (CSS) для стиля и макета.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-128">Between the <STYLE> and </STYLE> tags, you can define several Cascading Style Sheet (CSS) selectors for style and layout.</span></span> <span data-ttu-id="f3c0b-129">Свойства стиля, такие как шрифты, размеры и выравнивание, можно настроить таким образом, чтобы обеспечить широкие возможности для пользователей, а также повысить уровень доступности.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-129">Style properties such as fonts, sizes, and alignments can be customized to provide a rich user experience while also promoting accessibility.</span></span> <span data-ttu-id="f3c0b-130">Например, определение класса начертания больших текстовых шрифтов может улучшить удобочитаемость для пользователей, которые испытывают трудности при чтении мелкого текста.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-130">For example, defining a large text font style class can improve the readability for users who have difficulty reading small text.</span></span> <span data-ttu-id="f3c0b-131">Кроме того, определяя несколько различных классов языка, вы можете помочь международным пользователям лучше понять цифровые мультимедийные данные.</span><span class="sxs-lookup"><span data-stu-id="f3c0b-131">In addition, by defining several different language classes, you can help international users better understand the digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3c0b-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f3c0b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c0b-133">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="f3c0b-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




