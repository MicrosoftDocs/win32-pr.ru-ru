---
description: Тип расположения оглавления
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Тип расположения оглавления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692788"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="79468-103">Тип расположения оглавления</span><span class="sxs-lookup"><span data-stu-id="79468-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="79468-104">Некоторые методы интерфейса [**итокпарсер**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) имеют параметр с именем *енумтокпостипе* , имеющий тип [**перечислимого \_ \_ типа торговых терминалов**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span><span class="sxs-lookup"><span data-stu-id="79468-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="79468-105">Этот параметр указывает позицию в файле мультимедиа, где хранится оглавление.</span><span class="sxs-lookup"><span data-stu-id="79468-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="79468-106">Целью было то, что оглавление может храниться либо в заголовке файла, либо в тексте файла как объект верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="79468-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="79468-107">Эта функция пока не реализована.</span><span class="sxs-lookup"><span data-stu-id="79468-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="79468-108">В настоящее время таблицы содержимого могут храниться только как объекты верхнего уровня, поэтому для параметра *енумтокпостипе* необходимо всегда задавать **TOC \_ \_ топлевелобжект**.</span><span class="sxs-lookup"><span data-stu-id="79468-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="79468-109">Если для *енумтокпостипе* задано значение почтовых **\_ \_ головок**, метод возвратит **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="79468-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="79468-110">Следующие методы имеют параметр *енумтокпостипе* .</span><span class="sxs-lookup"><span data-stu-id="79468-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="79468-111">**жеттоккаунт**</span><span class="sxs-lookup"><span data-stu-id="79468-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="79468-112">**жеттокбиндекс**</span><span class="sxs-lookup"><span data-stu-id="79468-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="79468-113">**жеттокбитипе**</span><span class="sxs-lookup"><span data-stu-id="79468-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="79468-114">**аддток**</span><span class="sxs-lookup"><span data-stu-id="79468-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="79468-115">**ремоветокбиндекс**</span><span class="sxs-lookup"><span data-stu-id="79468-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="79468-116">**ремоветокбитипе**</span><span class="sxs-lookup"><span data-stu-id="79468-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="79468-117">См. также</span><span class="sxs-lookup"><span data-stu-id="79468-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79468-118">Справочное руководством по программированию синтаксического анализатора содержимого</span><span class="sxs-lookup"><span data-stu-id="79468-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



