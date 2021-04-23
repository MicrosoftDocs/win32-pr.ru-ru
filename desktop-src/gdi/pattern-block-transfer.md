---
description: Имя функции Патблт (сокращение для перемещения блока шаблона) подразумевает, что эта функция просто реплицирует кисть (или шаблон) до тех пор, пока не будет заполнен указанный прямоугольник.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Перенос блока шаблона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997334"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="52bae-103">Перенос блока шаблона</span><span class="sxs-lookup"><span data-stu-id="52bae-103">Pattern Block Transfer</span></span>

<span data-ttu-id="52bae-104">Имя функции [**патблт**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (сокращение для перемещения блока шаблона) подразумевает, что эта функция просто реплицирует кисть (или шаблон) до тех пор, пока не будет заполнен указанный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="52bae-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="52bae-105">Однако функция на самом деле гораздо эффективнее.</span><span class="sxs-lookup"><span data-stu-id="52bae-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="52bae-106">Перед репликацией кисти объединяет данные цвета для шаблона с данными цвета для существующих пикселей на дисплее видео с помощью операции растрового изображения (верхнем).</span><span class="sxs-lookup"><span data-stu-id="52bae-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="52bae-107">ВЕРХНЕМ — это битовая операция, которая применяется к битам данных цвета реплицированной кисти и битам цветовых данных для целевого прямоугольника на устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="52bae-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="52bae-108">256 РоПС; Однако функция **патблт** распознает только те, для которых требуется шаблон и назначение (а не те, которые нуждаются в источнике).</span><span class="sxs-lookup"><span data-stu-id="52bae-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="52bae-109">В следующей таблице приведены наиболее распространенные РоПС.</span><span class="sxs-lookup"><span data-stu-id="52bae-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="52bae-110">ВЕРХНЕМ</span><span class="sxs-lookup"><span data-stu-id="52bae-110">ROP</span></span>       | <span data-ttu-id="52bae-111">Описание</span><span class="sxs-lookup"><span data-stu-id="52bae-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52bae-112">паткопи</span><span class="sxs-lookup"><span data-stu-id="52bae-112">PATCOPY</span></span>   | <span data-ttu-id="52bae-113">Копирует шаблон в битовую карту назначения.</span><span class="sxs-lookup"><span data-stu-id="52bae-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="52bae-114">патинверт</span><span class="sxs-lookup"><span data-stu-id="52bae-114">PATINVERT</span></span> | <span data-ttu-id="52bae-115">Объединяет целевое битовое изображение с шаблоном с помощью логического оператора XOR.</span><span class="sxs-lookup"><span data-stu-id="52bae-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="52bae-116">дстинверт</span><span class="sxs-lookup"><span data-stu-id="52bae-116">DSTINVERT</span></span> | <span data-ttu-id="52bae-117">Инвертирует точечный рисунок назначения.</span><span class="sxs-lookup"><span data-stu-id="52bae-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="52bae-118">Черная</span><span class="sxs-lookup"><span data-stu-id="52bae-118">BLACKNESS</span></span> | <span data-ttu-id="52bae-119">Преобразует все выходные данные в двоичные нули.</span><span class="sxs-lookup"><span data-stu-id="52bae-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="52bae-120">вхитенесс</span><span class="sxs-lookup"><span data-stu-id="52bae-120">WHITENESS</span></span> | <span data-ttu-id="52bae-121">Включает все выходные данные в двоичные.</span><span class="sxs-lookup"><span data-stu-id="52bae-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="52bae-122">Дополнительные сведения см. в разделе [коды растровых операций](raster-operation-codes.md).</span><span class="sxs-lookup"><span data-stu-id="52bae-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



