---
title: Использование границ в пакетах загрузки Windows Media (устарело)
description: Использование границ в пакетах загрузки Windows Media (устарело)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Метафайлы Windows Media, пакеты загрузки Windows Media
- Проигрыватель Windows Media, пакеты загрузки Windows Media
- Метафайлы, пакеты загрузки Windows Media
- Windows Media, Загрузка пакетов Windows Media
- границы, сведения
- Пакеты загрузки Windows Media, границы
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411039"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="b21cb-109">Использование границ в пакетах загрузки Windows Media (устарело)</span><span class="sxs-lookup"><span data-stu-id="b21cb-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="b21cb-110">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="b21cb-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="b21cb-111">С помощью границ можно создать настраиваемый графический пользовательский интерфейс для упакованного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b21cb-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="b21cb-112">Эта граница может включать такие элементы, как изображения, интерактивные элементы управления и ссылки на веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="b21cb-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="b21cb-113">Границы можно использовать в тех случаях, когда требуется добавить дополнительное значение в упакованное содержимое, например для фирменной символики или рекламы.</span><span class="sxs-lookup"><span data-stu-id="b21cb-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="b21cb-114">После того как пользователи скачивают и открывают пакет загрузки Windows Media, проигрыватель Windows Media автоматически отображает пользовательскую границу при воспроизведении упакованного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b21cb-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="b21cb-115">В отличие от обложки, которая позволяет пользователям полностью заменить пользовательский интерфейс проигрывателя Windows Media, граница отображается только **в области "текущий" проигрывателя** в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="b21cb-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="b21cb-116">Тем не менее те же средства и технологии, которые используются для создания обложек, также используются для создания границ.</span><span class="sxs-lookup"><span data-stu-id="b21cb-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="b21cb-117">На следующем рисунке показана граница.</span><span class="sxs-lookup"><span data-stu-id="b21cb-117">The following illustration shows a border.</span></span>

![отображаемая граница Windows Media Player 10](images/border-v10.png)

<span data-ttu-id="b21cb-119">Важно понимать основные методы создания обложки, прежде чем пытаться создать границу.</span><span class="sxs-lookup"><span data-stu-id="b21cb-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="b21cb-120">Программирование границ осуществляется с помощью двух языков программирования: язык XML (XML) и Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="b21cb-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="b21cb-121">XML используется для определения элементов интерфейса, таких как кнопки, ползунки и текстовые поля.</span><span class="sxs-lookup"><span data-stu-id="b21cb-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="b21cb-122">Вам не нужно понимать все детали XML, так как вам не нужно писать новые элементы кода XML. можно просто использовать те, которые предоставляются проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b21cb-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="b21cb-123">Хотя для создания границ JScript не требуется, ее можно использовать для предоставления дополнительных функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="b21cb-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="b21cb-124">Сжатый файл границ с расширением WMZ включает файл определения границы с расширением WMS и все файлы изображений, используемые в границах.</span><span class="sxs-lookup"><span data-stu-id="b21cb-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="b21cb-125">Чтобы включить границу в пакет загрузки Windows Media, просто создайте границу и сослаться на эту границу в списке воспроизведения метафайла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b21cb-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="b21cb-126">Файл границ загружается в проигрыватель Windows Media после того, как проигрыватель анализирует метафайл и интерпретирует элемент **Skin** , который ссылается на эту границу.</span><span class="sxs-lookup"><span data-stu-id="b21cb-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="b21cb-127">Элемент **Skin** используется только для границ, а атрибут href элемента **Skin** может ссылаться только на одну обложку для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="b21cb-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b21cb-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b21cb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b21cb-129">**Границы для проигрывателя Windows Media (не рекомендуется)**</span><span class="sxs-lookup"><span data-stu-id="b21cb-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="b21cb-130">**Пакеты загрузки Windows Media (устарели)**</span><span class="sxs-lookup"><span data-stu-id="b21cb-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="b21cb-131">**Обложки проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b21cb-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




