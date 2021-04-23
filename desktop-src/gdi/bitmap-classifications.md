---
description: Классификации битовых карт
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Классификации битовых карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263699"
---
# <a name="bitmap-classifications"></a><span data-ttu-id="20d5d-103">Классификации битовых карт</span><span class="sxs-lookup"><span data-stu-id="20d5d-103">Bitmap Classifications</span></span>

<span data-ttu-id="20d5d-104">Существует два класса точечных рисунков:</span><span class="sxs-lookup"><span data-stu-id="20d5d-104">There are two classes of bitmaps:</span></span>

-   <span data-ttu-id="20d5d-105">[Аппаратно-независимые точечные рисунки](device-independent-bitmaps.md) (DIB).</span><span class="sxs-lookup"><span data-stu-id="20d5d-105">[Device-independent bitmaps](device-independent-bitmaps.md) (DIB).</span></span> <span data-ttu-id="20d5d-106">Формат файла DIB предназначен для того, чтобы обеспечить загрузку и отображение точечной графики, созданной с помощью одного приложения, в другом приложении, тем самым оставив тот же внешний вид, что и оригинал.</span><span class="sxs-lookup"><span data-stu-id="20d5d-106">The DIB file format was designed to ensure that bitmapped graphics created using one application can be loaded and displayed in another application, retaining the same appearance as the original.</span></span>

-   <span data-ttu-id="20d5d-107">Аппаратно [-зависимые точечные рисунки](device-dependent-bitmaps.md) (DDB), также известные как точечные рисунки GDI, являются единственными точечными рисунками, доступными в ранних версиях 16-разрядных операционных систем Microsoft Windows (до версии 3,0).</span><span class="sxs-lookup"><span data-stu-id="20d5d-107">[Device-dependent bitmaps](device-dependent-bitmaps.md) (DDB), also known as GDI bitmaps, were the only bitmaps available in early versions of 16-bit Microsoft Windows (prior to version 3.0).</span></span> <span data-ttu-id="20d5d-108">Тем не менее, по мере увеличения числа доступных устройств отображения, в том числе с увеличением, некоторые из них могут быть устранены только с помощью DIB.</span><span class="sxs-lookup"><span data-stu-id="20d5d-108">However, as display technology improved and as the variety of available display devices increased, certain inherent problems surfaced which could only be solved using DIBs.</span></span> <span data-ttu-id="20d5d-109">Например, не существовал метод хранения (или извлечения) разрешения типа отображения, на котором был создан точечный рисунок, поэтому приложение для рисования не может быстро определить, подходит ли точечный рисунок для типа видеоустройства, на котором выполнялось приложение.</span><span class="sxs-lookup"><span data-stu-id="20d5d-109">For example, there was no method of storing (or retrieving) the resolution of the display type on which a bitmap was created, so a drawing application could not quickly determine whether a bitmap was suitable for the type of video display device on which the application was running.</span></span>

    <span data-ttu-id="20d5d-110">Несмотря на эти проблемы, Ддбс (также известные как совместимые точечные рисунки) по-прежнему полезны для повышения производительности GDI и других ситуаций.</span><span class="sxs-lookup"><span data-stu-id="20d5d-110">Despite these problems, DDBs (also known as compatible bitmaps) are still useful for better GDI performance and for other situations.</span></span>

 

 



