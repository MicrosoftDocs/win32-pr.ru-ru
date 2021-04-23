---
title: Форматы данных и передачи мультимедиа
description: Форматы данных и передачи мультимедиа
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "104070843"
---
# <a name="data-formats-and-transfer-media"></a><span data-ttu-id="1af22-103">Форматы данных и передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1af22-103">Data Formats and Transfer Media</span></span>

<span data-ttu-id="1af22-104">Большинство платформ, в том числе Windows, определяют стандартный протокол для передачи данных между приложениями на основе набора функций, называемых буфером обмена.</span><span class="sxs-lookup"><span data-stu-id="1af22-104">Most platforms, including Windows, define a standard protocol for transferring data between applications, based on a set of functions called the clipboard.</span></span> <span data-ttu-id="1af22-105">Приложения, использующие эти функции, могут обмениваться данными, даже если их собственные форматы данных различаются.</span><span class="sxs-lookup"><span data-stu-id="1af22-105">Applications using these functions can share data even if their native data formats are wildly different.</span></span> <span data-ttu-id="1af22-106">Как правило, эти буферы обмена имеют два серьезных недостатка, которые пропреодолеть модель COM.</span><span class="sxs-lookup"><span data-stu-id="1af22-106">Generally, these clipboards have two significant shortcomings that COM has overcome.</span></span>

<span data-ttu-id="1af22-107">Во-первых, в описаниях данных используется только идентификатор формата, например один 16-разрядный идентификатор формата буфера обмена в Windows, что означает, что буфер обмена может описывать только структуру данных, то есть порядок битов.</span><span class="sxs-lookup"><span data-stu-id="1af22-107">First, data descriptions use only a format identifier, such as the single 16-bit clipboard format identifier on Windows, which means the clipboard can only describe the structure of its data, that is, the ordering of the bits.</span></span> <span data-ttu-id="1af22-108">Он может сообщить: «у меня есть точечный рисунок» или есть текст «», но он не может указывать целевые устройства, для которых состоят данные, какие представления или аспекты самих данных могут предоставляться или какие носители лучше всего подходят для его передачи.</span><span class="sxs-lookup"><span data-stu-id="1af22-108">It can report, "I have a bitmap" "or I have some text," but it cannot specify the target devices for which the data is composed, which views or aspects of itself the data can provide, or which storage media are best suited for its transfer.</span></span> <span data-ttu-id="1af22-109">Например, он не может сообщить: «у меня есть Текстовая строка, хранящаяся в глобальной памяти и отформатированная для представления на экране или на принтере» или «у меня есть растровое изображение эскиза, отображаемое для принтера с точечной матрицей 100 dpi и сохраненное как файл на диске».</span><span class="sxs-lookup"><span data-stu-id="1af22-109">For example, it cannot report, "I have a string of text that is stored in global memory and formatted for presentation either on screen or on a printer" or "I have a thumbnail sketch bitmap rendered for a 100 dpi dot-matrix printer and stored as a disk file."</span></span>

<span data-ttu-id="1af22-110">Во-вторых, все передачи данных с помощью буфера обмена обычно происходят через глобальную память.</span><span class="sxs-lookup"><span data-stu-id="1af22-110">Second, all data transfers using the clipboard generally occur through global memory.</span></span> <span data-ttu-id="1af22-111">Использование глобальной памяти достаточно эффективно для небольших объемов данных, но ужасно неэффективно для больших объемов, таких как мультимедийный объект размером 20 МБ.</span><span class="sxs-lookup"><span data-stu-id="1af22-111">Using global memory is reasonably efficient for small amounts of data but horribly inefficient for large amounts, such as a 20 MB multimedia object.</span></span> <span data-ttu-id="1af22-112">Глобальная память работает слишком долго для больших объектов данных, размер которой требует значительного переключения на виртуальную память на диске.</span><span class="sxs-lookup"><span data-stu-id="1af22-112">Global memory is slow for a large data object, whose size requires considerable swapping to virtual memory on disk.</span></span> <span data-ttu-id="1af22-113">В случаях, когда данные, которыми вы обмениваетесь, обычно находятся в основном на диске, принудительное применение этого узкого места виртуальной памяти является очень неэффективным.</span><span class="sxs-lookup"><span data-stu-id="1af22-113">In cases where the data being exchanged is going to reside mostly on disk anyway, forcing it through this virtual-memory bottleneck is highly inefficient.</span></span> <span data-ttu-id="1af22-114">Лучшим способом будет полностью пропускать глобальную память и просто передавать данные непосредственно на диск.</span><span class="sxs-lookup"><span data-stu-id="1af22-114">A better way would skip global memory entirely and simply transfer the data directly to disk.</span></span>

<span data-ttu-id="1af22-115">Чтобы решить эти проблемы, COM предоставляет две структуры данных: [**форматетк**](/windows/win32/api/objidl/ns-objidl-formatetc) и [**стгмедиум**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span><span class="sxs-lookup"><span data-stu-id="1af22-115">To alleviate these problems, COM provides two data structures: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) and [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span></span> <span data-ttu-id="1af22-116">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1af22-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1af22-117">Структура ФОРМАТЕТК</span><span class="sxs-lookup"><span data-stu-id="1af22-117">The FORMATETC Structure</span></span>](the-formatetc-structure.md)
-   [<span data-ttu-id="1af22-118">Структура СТГМЕДИУМ</span><span class="sxs-lookup"><span data-stu-id="1af22-118">The STGMEDIUM Structure</span></span>](the-stgmedium-structure.md)

## <a name="related-topics"></a><span data-ttu-id="1af22-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1af22-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1af22-120">Передача данных</span><span class="sxs-lookup"><span data-stu-id="1af22-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




