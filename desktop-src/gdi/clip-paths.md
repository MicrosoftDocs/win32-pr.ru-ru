---
description: Как и в области обрезки, путь отсечения — это другой объект Graphics, который приложение может выбрать в контексте устройства.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Пути обрезки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985045"
---
# <a name="clip-paths"></a><span data-ttu-id="b4243-103">Пути обрезки</span><span class="sxs-lookup"><span data-stu-id="b4243-103">Clip Paths</span></span>

<span data-ttu-id="b4243-104">Как и в области обрезки, путь отсечения — это другой объект Graphics, который приложение может выбрать в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="b4243-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="b4243-105">В отличие от области отсечения, путь обрезки всегда создается приложением и используется для обрезки до одной или нескольких нестандартных фигур.</span><span class="sxs-lookup"><span data-stu-id="b4243-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="b4243-106">Например, приложение может использовать линии и кривые, которые формируют контуры символов в текстовой строке для определения пути обрезки.</span><span class="sxs-lookup"><span data-stu-id="b4243-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="b4243-107">Чтобы создать путь к обрезке, сначала необходимо создать путь, описывающий требуемую нерегулярную форму.</span><span class="sxs-lookup"><span data-stu-id="b4243-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="b4243-108">Пути создаются путем вызова соответствующих функций графического интерфейса графических устройств (GDI) после вызова функции [**бегинпас**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) и перед вызовом функции [**ендпас**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="b4243-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="b4243-109">Эта коллекция функций называется скобкой пути.</span><span class="sxs-lookup"><span data-stu-id="b4243-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="b4243-110">Дополнительные сведения о путях и скобках пути см. в разделе [paths](paths.md).</span><span class="sxs-lookup"><span data-stu-id="b4243-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="b4243-111">После создания пути его можно преобразовать в путь обрезки, вызвав функцию [**селектклиппас**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , определив контекст устройства и указав режим использования.</span><span class="sxs-lookup"><span data-stu-id="b4243-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="b4243-112">Режим использования определяет, как система объединяет новый путь к клипу с исходной областью отсечения контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="b4243-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="b4243-113">В следующей таблице описаны режимы использования.</span><span class="sxs-lookup"><span data-stu-id="b4243-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="b4243-114">Режим</span><span class="sxs-lookup"><span data-stu-id="b4243-114">Mode</span></span>      | <span data-ttu-id="b4243-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b4243-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4243-116">РГН \_ и</span><span class="sxs-lookup"><span data-stu-id="b4243-116">RGN\_AND</span></span>  | <span data-ttu-id="b4243-117">Путь обрезки включает пересечение (перекрывающиеся области) области отсечения контекста устройства и текущего пути.</span><span class="sxs-lookup"><span data-stu-id="b4243-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="b4243-118">\_копирование РГН</span><span class="sxs-lookup"><span data-stu-id="b4243-118">RGN\_COPY</span></span> | <span data-ttu-id="b4243-119">Путь к обрезку — это текущий путь.</span><span class="sxs-lookup"><span data-stu-id="b4243-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="b4243-120">РГН \_ diff</span><span class="sxs-lookup"><span data-stu-id="b4243-120">RGN\_DIFF</span></span> | <span data-ttu-id="b4243-121">Путь к обрезку включает область обрезки контекста устройства с любыми пересекающимися частями текущего пути.</span><span class="sxs-lookup"><span data-stu-id="b4243-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="b4243-122">РГН \_ или</span><span class="sxs-lookup"><span data-stu-id="b4243-122">RGN\_OR</span></span>   | <span data-ttu-id="b4243-123">Путь обрезки включает объединение (Объединенные области) области отсечения контекста устройства и текущий путь.</span><span class="sxs-lookup"><span data-stu-id="b4243-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="b4243-124">РГН \_ XOR</span><span class="sxs-lookup"><span data-stu-id="b4243-124">RGN\_XOR</span></span>  | <span data-ttu-id="b4243-125">Путь обрезки включает объединение области отсечения контекста устройства и текущего пути, но исключает пересечение.</span><span class="sxs-lookup"><span data-stu-id="b4243-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 



