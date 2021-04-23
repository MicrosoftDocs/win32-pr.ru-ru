---
description: Ограничивающим прямоугольником всех мониторов является виртуальный экран. Рабочий стол охватывает виртуальный экран, а не один монитор. На следующем рисунке показано возможное расположение трех мониторов.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Виртуальный экран
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997930"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="c7b76-105">Виртуальный экран</span><span class="sxs-lookup"><span data-stu-id="c7b76-105">The Virtual Screen</span></span>

<span data-ttu-id="c7b76-106">Ограничивающим прямоугольником всех мониторов является *виртуальный экран*.</span><span class="sxs-lookup"><span data-stu-id="c7b76-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="c7b76-107">Рабочий стол охватывает виртуальный экран, а не один монитор.</span><span class="sxs-lookup"><span data-stu-id="c7b76-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="c7b76-108">На следующем рисунке показано возможное расположение трех мониторов.</span><span class="sxs-lookup"><span data-stu-id="c7b76-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![Иллюстрация, демонстрирующая три поля, представляющие мониторы, расположенные внутри поля, представляющего виртуальный экран](images/multimon-1.png)

<span data-ttu-id="c7b76-110">*Основной монитор* содержит источник (0, 0).</span><span class="sxs-lookup"><span data-stu-id="c7b76-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="c7b76-111">Это относится к совместимости с существующими приложениями, которые предполагают наличие монитора с источником.</span><span class="sxs-lookup"><span data-stu-id="c7b76-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="c7b76-112">Однако основной монитор не обязательно должен находиться в левом верхнем углу виртуального экрана.</span><span class="sxs-lookup"><span data-stu-id="c7b76-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="c7b76-113">На рис. 1 он находится ближе к центру.</span><span class="sxs-lookup"><span data-stu-id="c7b76-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="c7b76-114">Если основной монитор находится не в левом верхнем углу виртуального экрана, части виртуального экрана имеют отрицательные координаты.</span><span class="sxs-lookup"><span data-stu-id="c7b76-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="c7b76-115">Так как расположение мониторов устанавливается пользователем, все приложения должны быть спроектированы для работы с отрицательными координатами.</span><span class="sxs-lookup"><span data-stu-id="c7b76-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="c7b76-116">Дополнительные сведения см. в разделе [рекомендации по нескольким мониторам для старых программ](multiple-monitor-considerations-for-older-programs.md).</span><span class="sxs-lookup"><span data-stu-id="c7b76-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="c7b76-117">Координаты виртуального экрана представлены 16-битным значением со знаком, так как из 16-разрядных значений содержатся в нескольких существующих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="c7b76-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="c7b76-118">Таким образом, границы виртуального экрана:</span><span class="sxs-lookup"><span data-stu-id="c7b76-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



