---
title: Время (мультимедиа Windows)
description: Временные свойства
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- Дравдиб, время
- Функция Дравдибтиме
- Дравдиб, отладка
- Отладка Дравдиб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488754"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="3aa21-107">Время (мультимедиа Windows)</span><span class="sxs-lookup"><span data-stu-id="3aa21-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="3aa21-108">В рамках отладки приложения можно получить сведения о количестве времени, необходимого для выполнения повторяющихся операций Дравдиб.</span><span class="sxs-lookup"><span data-stu-id="3aa21-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="3aa21-109">Функция [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) возвращает сведения о времени для следующих операций:</span><span class="sxs-lookup"><span data-stu-id="3aa21-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="3aa21-110">Рисование точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="3aa21-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="3aa21-111">Распаковка точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="3aa21-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="3aa21-112">Сглаживание точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="3aa21-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="3aa21-113">Растяжение растрового изображения</span><span class="sxs-lookup"><span data-stu-id="3aa21-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="3aa21-114">Передача точечного рисунка с помощью функции [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)</span><span class="sxs-lookup"><span data-stu-id="3aa21-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="3aa21-115">Передача точечного рисунка с помощью функции [**стретчдибитс**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)</span><span class="sxs-lookup"><span data-stu-id="3aa21-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="3aa21-116">После получения набора значений [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) сбрасывает количество и значение для каждой операции.</span><span class="sxs-lookup"><span data-stu-id="3aa21-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="3aa21-117">Функция [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) доступна только в отладочной версии функций дравдиб.</span><span class="sxs-lookup"><span data-stu-id="3aa21-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aa21-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3aa21-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aa21-119">Рендеринг изображений</span><span class="sxs-lookup"><span data-stu-id="3aa21-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
