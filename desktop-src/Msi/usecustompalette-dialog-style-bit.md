---
description: Если этот бит задан, изображения в диалоговом окне создаются с помощью пользовательской палитры (по одному на диалоговое окно, полученное от первого созданного элемента управления). Если бит не задан, изображения визуализируются с использованием палитры по умолчанию.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Бит стиля диалогового окна Усекустомпалетте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651162"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="b7805-104">Бит стиля диалогового окна Усекустомпалетте</span><span class="sxs-lookup"><span data-stu-id="b7805-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="b7805-105">Если этот бит задан, изображения в диалоговом окне создаются с помощью пользовательской палитры (по одному на диалоговое окно, полученное от первого созданного элемента управления).</span><span class="sxs-lookup"><span data-stu-id="b7805-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="b7805-106">Если бит не задан, изображения визуализируются с использованием палитры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7805-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="b7805-107">Как правило, этот бит устанавливается, если диалоговое окно содержит изображение со специальной палитрой или несколько изображений, совместно использующих пользовательскую палитру.</span><span class="sxs-lookup"><span data-stu-id="b7805-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="b7805-108">Если диалоговое окно содержит несколько изображений с разными палитрами, то бит указывать не следует.</span><span class="sxs-lookup"><span data-stu-id="b7805-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="b7805-109">В этом случае палитра по умолчанию, скорее всего, обеспечит удовлетворительный результат для всех изображений.</span><span class="sxs-lookup"><span data-stu-id="b7805-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="b7805-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b7805-110">Value</span></span>



| <span data-ttu-id="b7805-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="b7805-111">Decimal</span></span> | <span data-ttu-id="b7805-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="b7805-112">Hexadecimal</span></span> | <span data-ttu-id="b7805-113">Константа</span><span class="sxs-lookup"><span data-stu-id="b7805-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="b7805-114">64</span><span class="sxs-lookup"><span data-stu-id="b7805-114">64</span></span>      | <span data-ttu-id="b7805-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="b7805-115">0x00000040</span></span>  | <span data-ttu-id="b7805-116">**мсидбдиалогаттрибутесусекустомпалетте**</span><span class="sxs-lookup"><span data-stu-id="b7805-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



