---
title: Создание пакета загрузки Windows Media (не рекомендуется)
description: Создание пакета загрузки Windows Media (не рекомендуется)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Метафайлы Windows Media, пакеты загрузки Windows Media
- Проигрыватель Windows Media, пакеты загрузки Windows Media
- Метафайлы, пакеты загрузки Windows Media
- Windows Media, Загрузка пакетов Windows Media
- Пакеты загрузки Windows Media, создание
- Создание пакетов загрузки Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068180"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="ed5a1-109">Создание пакета загрузки Windows Media (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="ed5a1-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="ed5a1-110">Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="ed5a1-111">Выполните следующие действия, чтобы создать пакет загрузки Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="ed5a1-112">**Создайте границу.**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-112">**Create a border.**</span></span> <span data-ttu-id="ed5a1-113">Используйте те же методы, которые используются для создания обложки для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="ed5a1-114">Разработайте границу таким образом, чтобы изменение размера проигрывателя Windows Media не насмарку композиции элементов границ.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="ed5a1-115">Например, используйте сплошной цвет или визуализацию в качестве фона, так как они будут масштабироваться при изменении размера проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="ed5a1-116">**Сжатие содержимого границы.**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-116">**Compress the border contents.**</span></span> <span data-ttu-id="ed5a1-117">Создайте сжатую папку (с расширением ZIP), которая содержит файлы границ: Images, JScript и файл определения обложки с расширением WMS.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="ed5a1-118">Переименуйте сжатый файл, чтобы он был иметь расширение WMZ.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="ed5a1-119">**Написание метафайла Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="ed5a1-120">Проигрыватель Windows Media не загрузит границу, пока не будет создан метафайл Windows Media с расширением. ASX, реализующим элемент **Skin** .</span><span class="sxs-lookup"><span data-stu-id="ed5a1-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="ed5a1-121">Метафайл также можно использовать для создания списка воспроизведения, который описывает содержимое, входящее в пакет.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="ed5a1-122">**Соберите содержимое.**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-122">**Assemble your content.**</span></span> <span data-ttu-id="ed5a1-123">Вставьте все файлы, которые вы хотите использовать, в папку.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="ed5a1-124">Сюда входят звуковые файлы, видеофайлы, метафайлы и файлы определения границы.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="ed5a1-125">**Создайте пакет.**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-125">**Create the package.**</span></span> <span data-ttu-id="ed5a1-126">Создайте сжатую папку (с расширением ZIP), содержащую файл границ, файлы содержимого и метафайл.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="ed5a1-127">Измените расширение имени файла этого ZIP-файла на расширение имени файла WMD.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="ed5a1-128">**Опубликуйте пакет на веб-сайте.**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-128">**Post the package to a website.**</span></span> <span data-ttu-id="ed5a1-129">Завершенный пакет готов к отправке на веб-сайт и скачан пользователями.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed5a1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ed5a1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed5a1-131">**Пакеты загрузки Windows Media (устарели)**</span><span class="sxs-lookup"><span data-stu-id="ed5a1-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




