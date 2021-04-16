---
description: ICE56 проверяет, что структура каталогов MSI-файла имеет единственный корневой каталог, что корень является свойством TARGETDIR, а значение свойства SourceDir — в столбце Дефаултдир таблицы Directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664035"
---
# <a name="ice56"></a><span data-ttu-id="7eea3-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="7eea3-103">ICE56</span></span>

<span data-ttu-id="7eea3-104">ICE56 проверяет, что структура каталогов MSI-файла имеет единственный корневой каталог, что корень является свойством [**targetDir**](targetdir.md) , а значение свойства [**SourceDir**](sourcedir.md) — в столбце дефаултдир [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="7eea3-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="7eea3-105">Если MSI-файл имеет несколько корней или указывает корень, отличный от [**targetDir**](targetdir.md), [Административная установка](administrative-installation.md) не создает правильный административный образ.</span><span class="sxs-lookup"><span data-stu-id="7eea3-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="7eea3-106">Обратите внимание, что пустые каталоги не проверяются с помощью ICE56.</span><span class="sxs-lookup"><span data-stu-id="7eea3-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="7eea3-107">Структура каталогов проходит проверку с несколькими корневыми каталогами, если лишние каталоги пусты.</span><span class="sxs-lookup"><span data-stu-id="7eea3-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="7eea3-108">Результат</span><span class="sxs-lookup"><span data-stu-id="7eea3-108">Result</span></span>

<span data-ttu-id="7eea3-109">ICE56 отправляет сообщение об ошибке, если MSI не имеет одного корня, [**targetDir**](targetdir.md)или если [**SourceDir**](sourcedir.md) не указан в столбце дефаултдир [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="7eea3-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="7eea3-110">Пример</span><span class="sxs-lookup"><span data-stu-id="7eea3-110">Example</span></span>

<span data-ttu-id="7eea3-111">ICE56 сообщает о следующих ошибках в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="7eea3-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="7eea3-112">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="7eea3-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="7eea3-113">Каталог</span><span class="sxs-lookup"><span data-stu-id="7eea3-113">Directory</span></span> | <span data-ttu-id="7eea3-114">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="7eea3-114">Directory\_Parent</span></span> | <span data-ttu-id="7eea3-115">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="7eea3-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="7eea3-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="7eea3-116">TARGETDIR</span></span> |                   | <span data-ttu-id="7eea3-117">Temp</span><span class="sxs-lookup"><span data-stu-id="7eea3-117">Temp</span></span>       |
| <span data-ttu-id="7eea3-118">Root2</span><span class="sxs-lookup"><span data-stu-id="7eea3-118">Root2</span></span>     | <span data-ttu-id="7eea3-119">Root2</span><span class="sxs-lookup"><span data-stu-id="7eea3-119">Root2</span></span>             | <span data-ttu-id="7eea3-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="7eea3-120">SourceDir</span></span>  |



 

<span data-ttu-id="7eea3-121">Чтобы исправить первую ошибку, корневой элемент [**targetDir**](targetdir.md) должен иметь значение дефаултдир, равное [**SourceDir**](sourcedir.md).</span><span class="sxs-lookup"><span data-stu-id="7eea3-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="7eea3-122">SOURCEDIR также принимается.</span><span class="sxs-lookup"><span data-stu-id="7eea3-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="7eea3-123">Можно сделать так, чтобы параметр **targetDir** был родителем второго корня и использовал значение "." в столбце дефаултдир.</span><span class="sxs-lookup"><span data-stu-id="7eea3-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="7eea3-124">Дополнительные сведения см. в [таблице Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7eea3-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="7eea3-125">Чтобы устранить вторую ошибку, структура каталогов должна иметь только один корень с именем [**targetDir**](targetdir.md).</span><span class="sxs-lookup"><span data-stu-id="7eea3-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eea3-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7eea3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eea3-127">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="7eea3-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



