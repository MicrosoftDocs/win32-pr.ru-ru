---
description: Компоненты BLOB-объектов
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Компоненты BLOB-объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265653"
---
# <a name="blob-components"></a><span data-ttu-id="58bfa-103">Компоненты BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="58bfa-103">BLOB Components</span></span>

<span data-ttu-id="58bfa-104">Большой двоичный объект (BLOB) включает следующие иерархические компоненты:</span><span class="sxs-lookup"><span data-stu-id="58bfa-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="58bfa-105">Владельцы</span><span class="sxs-lookup"><span data-stu-id="58bfa-105">Owners</span></span>
-   <span data-ttu-id="58bfa-106">Категории</span><span class="sxs-lookup"><span data-stu-id="58bfa-106">Categories</span></span>
-   <span data-ttu-id="58bfa-107">Теги</span><span class="sxs-lookup"><span data-stu-id="58bfa-107">Tags</span></span>
-   <span data-ttu-id="58bfa-108">Значения</span><span class="sxs-lookup"><span data-stu-id="58bfa-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="58bfa-109">Текстовое представление</span><span class="sxs-lookup"><span data-stu-id="58bfa-109">Textual Representation</span></span>

<span data-ttu-id="58bfa-110">Для удобства большие двоичные объекты отображаются в формате владелец: Категория: Тег: значение, в котором они отображаются при сохранении в файл.</span><span class="sxs-lookup"><span data-stu-id="58bfa-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="58bfa-111">Внутренняя структура большого двоичного объекта является непрозрачной, так как представляет собой указатели и таблицы.</span><span class="sxs-lookup"><span data-stu-id="58bfa-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="58bfa-112">Например, ниже приведена запись из большого двоичного объекта, который можно использовать для настройки НПП:</span><span class="sxs-lookup"><span data-stu-id="58bfa-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="58bfa-113">Владелец — НПП.</span><span class="sxs-lookup"><span data-stu-id="58bfa-113">The Owner is NPP.</span></span> <span data-ttu-id="58bfa-114">Категория — configure, тег — BufferSize, а значение — 32768.</span><span class="sxs-lookup"><span data-stu-id="58bfa-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 



