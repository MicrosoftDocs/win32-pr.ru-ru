---
description: Флаг возможностей драйвера.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701194"
---
# <a name="d3denum"></a><span data-ttu-id="7d6e6-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="7d6e6-103">D3DENUM</span></span>

<span data-ttu-id="7d6e6-104">Флаг возможностей драйвера.</span><span class="sxs-lookup"><span data-stu-id="7d6e6-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d6e6-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="7d6e6-105">#define</span></span></td>
<td><span data-ttu-id="7d6e6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7d6e6-106">Value</span></span></td>
<td><span data-ttu-id="7d6e6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7d6e6-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d6e6-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="7d6e6-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="7d6e6-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="7d6e6-109">0x00000002L</span></span></td>
<td><span data-ttu-id="7d6e6-110">Тестирование драйвера лаборатории WHQL для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7d6e6-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="7d6e6-111">Это длительный тест, требующий снижения времени на одну секунду или две секунды.</span><span class="sxs-lookup"><span data-stu-id="7d6e6-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="7d6e6-112">Эта константа используется членом Вхкллевел <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7d6e6-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d6e6-113">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="7d6e6-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d6e6-114">D3DENUM_WHQL_LEVEL не рекомендуется использовать для Direct3D9Ex, работающих под управлением Windows Vista, Windows Server 2008, Windows 7 и Windows Server 2008 R2 (или более текущей операционной системы).</span><span class="sxs-lookup"><span data-stu-id="7d6e6-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="7d6e6-115">Любая из этих операционных систем возвращает 1 для уровня WHQL без проверки состояния драйвера.</span><span class="sxs-lookup"><span data-stu-id="7d6e6-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="7d6e6-116">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="7d6e6-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="7d6e6-117">Header</span><span class="sxs-lookup"><span data-stu-id="7d6e6-117">Header</span></span>                   | <span data-ttu-id="7d6e6-118">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="7d6e6-118">d3d9.h</span></span>     |
| <span data-ttu-id="7d6e6-119">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="7d6e6-119">Minimum operating system</span></span> | <span data-ttu-id="7d6e6-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7d6e6-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7d6e6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="7d6e6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d6e6-122">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="7d6e6-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




