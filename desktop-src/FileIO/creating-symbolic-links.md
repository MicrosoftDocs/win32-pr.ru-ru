---
description: Создайте символические ссылки, использующие абсолютный или относительный путь с помощью функции Креатесимболиклинк.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Создание символьных ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252b999b05004fd7735b16582783ef0c3afb0013
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387710"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="312a3-103">Создание символьных ссылок</span><span class="sxs-lookup"><span data-stu-id="312a3-103">Creating Symbolic Links</span></span>

<span data-ttu-id="312a3-104">Функция [**креатесимболиклинк**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) позволяет создавать символьные ссылки с помощью абсолютного или относительного пути.</span><span class="sxs-lookup"><span data-stu-id="312a3-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="312a3-105">Символьные ссылки могут быть либо абсолютными, либо относительными ссылками.</span><span class="sxs-lookup"><span data-stu-id="312a3-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="312a3-106">Абсолютные ссылки — это ссылки, указывающие каждую часть имени пути; относительные ссылки определяются относительно того, где относительные указатели находятся в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="312a3-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="312a3-107">Относительные ссылки указываются с использованием следующих соглашений:</span><span class="sxs-lookup"><span data-stu-id="312a3-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="312a3-108">Точка (.</span><span class="sxs-lookup"><span data-stu-id="312a3-108">Dot (.</span></span> <span data-ttu-id="312a3-109">и..) соглашения, например ".. \\ " Разрешает путь относительно родительского каталога.</span><span class="sxs-lookup"><span data-stu-id="312a3-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="312a3-110">Имена без косой черты ( \\ ) — например, "tmp" разрешает путь относительно текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="312a3-110">Names with no slashes (\\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="312a3-111">Относительный корень, например " \\ Windows \\ System32", разрешается в "*текущий диск*: \\ Windows \\ System32".</span><span class="sxs-lookup"><span data-stu-id="312a3-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="312a3-112">directory.</span><span class="sxs-lookup"><span data-stu-id="312a3-112">directory</span></span>
-   <span data-ttu-id="312a3-113">Текущий рабочий каталог — относительно. Например, если текущим рабочим каталогом является "C: \\ Windows \\ System32", "C:File.txt" разрешается в "c: \\ Windows \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="312a3-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="312a3-114">**Примечание**  .  Если указана ссылка относительно текущего рабочего каталога, она создается как абсолютная ссылка, так как текущий рабочий каталог обрабатывается на основе пользователя и потока.</span><span class="sxs-lookup"><span data-stu-id="312a3-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="312a3-115">Символьная ссылка также может содержать как точки соединения, так и подключенные папки в качестве части имени пути.</span><span class="sxs-lookup"><span data-stu-id="312a3-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="312a3-116">Символьные ссылки могут указывать непосредственно на удаленный файл или каталог, используя UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="312a3-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="312a3-117">Относительные символьные ссылки ограничены одним томом.</span><span class="sxs-lookup"><span data-stu-id="312a3-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="312a3-118">Пример абсолютной символьной ссылки</span><span class="sxs-lookup"><span data-stu-id="312a3-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="312a3-119">В этом примере исходный путь содержит компонент «*x*», который является абсолютной символьной ссылкой.</span><span class="sxs-lookup"><span data-stu-id="312a3-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="312a3-120">При обнаружении "*x*" фрагмент исходного пути вплоть до "*x*" полностью заменен на путь, на который указывает "*x*".</span><span class="sxs-lookup"><span data-stu-id="312a3-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="312a3-121">Оставшаяся часть пути после "*x*" добавляется к этому новому пути.</span><span class="sxs-lookup"><span data-stu-id="312a3-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="312a3-122">Теперь он становится измененным путем.</span><span class="sxs-lookup"><span data-stu-id="312a3-122">This now becomes the modified path.</span></span>

<span data-ttu-id="312a3-123">X: "C: \\ \\ \\ файл гаммы абслинк бета-версии Alpha \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="312a3-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="312a3-124">Ссылка: "Абслинк" сопоставляется с " \\ \\ мачинеб \\ Share"</span><span class="sxs-lookup"><span data-stu-id="312a3-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="312a3-125">Измененный путь: " \\ \\ мачинеб \\ \\ файл гаммы общего ресурса \\ "</span><span class="sxs-lookup"><span data-stu-id="312a3-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="312a3-126">Пример относительной символической ссылки</span><span class="sxs-lookup"><span data-stu-id="312a3-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="312a3-127">В этом примере исходный путь содержит компонент "*x*", который является относительным символом ссылки.</span><span class="sxs-lookup"><span data-stu-id="312a3-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="312a3-128">При обнаружении "*x*" "*x*" полностью заменяется новым фрагментом, на который указывает "*x*".</span><span class="sxs-lookup"><span data-stu-id="312a3-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="312a3-129">Оставшаяся часть пути после "*x*" добавляется к новому пути.</span><span class="sxs-lookup"><span data-stu-id="312a3-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="312a3-130">Все точки (..) в этом новом пути заменяют компоненты, которые отображаются перед точками (..).</span><span class="sxs-lookup"><span data-stu-id="312a3-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="312a3-131">Каждый набор точек заменяет предшествующий компонент.</span><span class="sxs-lookup"><span data-stu-id="312a3-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="312a3-132">Если число точек (..) превышает количество компонентов, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="312a3-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="312a3-133">В противном случае после завершения замены всех компонентов сохраняется последний измененный путь.</span><span class="sxs-lookup"><span data-stu-id="312a3-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="312a3-134">X: C: \\ альфа \\ - \\ \\ файл гаммы ссылки Beta \\</span><span class="sxs-lookup"><span data-stu-id="312a3-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="312a3-135">Ссылка: "связать" сопоставляется с ".. \\ . \\ " тета-</span><span class="sxs-lookup"><span data-stu-id="312a3-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="312a3-136">Измененный путь: "C: \\ альфа \\ Beta \\ .. \\ . \\ \\файл гаммы тета \\ "</span><span class="sxs-lookup"><span data-stu-id="312a3-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="312a3-137">Окончательный путь: "C: \\ тета \\ гамма- \\ файл"</span><span class="sxs-lookup"><span data-stu-id="312a3-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="312a3-138">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="312a3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="312a3-139">Символические ссылки</span><span class="sxs-lookup"><span data-stu-id="312a3-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="312a3-140">Жесткие связи и соединения</span><span class="sxs-lookup"><span data-stu-id="312a3-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="312a3-141">Именование файлов, путей и пространств имен</span><span class="sxs-lookup"><span data-stu-id="312a3-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



