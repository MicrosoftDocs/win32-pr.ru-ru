---
description: Расширенный метафайл — это массив записей.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Расширенные записи метафайлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984969"
---
# <a name="enhanced-metafile-records"></a><span data-ttu-id="b30eb-103">Расширенные записи метафайлов</span><span class="sxs-lookup"><span data-stu-id="b30eb-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="b30eb-104">Расширенный метафайл — это массив записей.</span><span class="sxs-lookup"><span data-stu-id="b30eb-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="b30eb-105">Запись метафайла — это [**енхметарекорд**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) структура переменной длины.</span><span class="sxs-lookup"><span data-stu-id="b30eb-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="b30eb-106">В начале каждой записи расширенного метафайла используется структура [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , которая содержит два члена.</span><span class="sxs-lookup"><span data-stu-id="b30eb-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="b30eb-107">Первый элемент, Итипе, определяет тип записи, то есть функцию GDI, параметры которой содержатся в записи.</span><span class="sxs-lookup"><span data-stu-id="b30eb-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="b30eb-108">Так как структуры имеют переменную length, другой элемент, Нсизе, содержит размер записи.</span><span class="sxs-lookup"><span data-stu-id="b30eb-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="b30eb-109">Сразу после элемента Нсизе остаются оставшиеся параметры функции GDI (если таковые имеются).</span><span class="sxs-lookup"><span data-stu-id="b30eb-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="b30eb-110">Оставшаяся часть структуры содержит дополнительные данные, зависящие от типа записи.</span><span class="sxs-lookup"><span data-stu-id="b30eb-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="b30eb-111">Первая запись в расширенном метафайле всегда является структурой [**енхметахеадер**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , которая является заголовком расширенного метафайла.</span><span class="sxs-lookup"><span data-stu-id="b30eb-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="b30eb-112">В заголовке указываются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b30eb-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="b30eb-113">Размер метафайла (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b30eb-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="b30eb-114">Размеры рамки изображения в единицах устройства</span><span class="sxs-lookup"><span data-stu-id="b30eb-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="b30eb-115">Размеры рамки изображения в единицах с 01 миллиметрами</span><span class="sxs-lookup"><span data-stu-id="b30eb-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="b30eb-116">Число записей в метафайле</span><span class="sxs-lookup"><span data-stu-id="b30eb-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="b30eb-117">Смещение к необязательному текстовому описанию</span><span class="sxs-lookup"><span data-stu-id="b30eb-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="b30eb-118">Размер дополнительной палитры</span><span class="sxs-lookup"><span data-stu-id="b30eb-118">Size of the optional palette</span></span>
-   <span data-ttu-id="b30eb-119">Разрешение исходного устройства в пикселях</span><span class="sxs-lookup"><span data-stu-id="b30eb-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="b30eb-120">Разрешение исходного устройства в миллиметрах</span><span class="sxs-lookup"><span data-stu-id="b30eb-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="b30eb-121">Необязательное текстовое описание может следовать за записью заголовка.</span><span class="sxs-lookup"><span data-stu-id="b30eb-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="b30eb-122">Текстовое описание описывает изображение и имя автора.</span><span class="sxs-lookup"><span data-stu-id="b30eb-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="b30eb-123">Необязательная палитра определяет цвета, используемые для создания расширенного метафайла.</span><span class="sxs-lookup"><span data-stu-id="b30eb-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="b30eb-124">Оставшиеся записи обозначают функции GDI, используемые для создания изображения.</span><span class="sxs-lookup"><span data-stu-id="b30eb-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="b30eb-125">Следующие шестнадцатеричные выходные данные соответствуют записи, формируемой для вызова функции [**сетмапмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .</span><span class="sxs-lookup"><span data-stu-id="b30eb-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="b30eb-126">Значение 0x00000011 указывает тип записи (соответствует \_ константе СЕТМАПМОДЕ EMR, определенной в файле вингди. h).</span><span class="sxs-lookup"><span data-stu-id="b30eb-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="b30eb-127">Значение 0x0000000C указывает длину записи в байтах.</span><span class="sxs-lookup"><span data-stu-id="b30eb-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="b30eb-128">Значение 0x00000004 определяет режим сопоставления (соответствует \_ константе mm лоенглиш, определенной в функции [**сетмапмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).</span><span class="sxs-lookup"><span data-stu-id="b30eb-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="b30eb-129">Список дополнительных типов записей см. в разделе [структуры метафайлов](metafile-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b30eb-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 



