---
description: Флаг возможностей драйвера.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829d03bf596c24bfb6b3443ace859629f723a664
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343267"
---
# <a name="d3denum"></a><span data-ttu-id="773d5-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="773d5-103">D3DENUM</span></span>

<span data-ttu-id="773d5-104">Флаг возможностей драйвера.</span><span class="sxs-lookup"><span data-stu-id="773d5-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="773d5-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="773d5-105">#define</span></span></td>
<td><span data-ttu-id="773d5-106">Значение</span><span class="sxs-lookup"><span data-stu-id="773d5-106">Value</span></span></td>
<td><span data-ttu-id="773d5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="773d5-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="773d5-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="773d5-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="773d5-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="773d5-109">0x00000002L</span></span></td>
<td><span data-ttu-id="773d5-110">Тестирование драйвера лаборатории WHQL для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="773d5-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="773d5-111">Это длительный тест, требующий снижения времени на одну секунду или две секунды.</span><span class="sxs-lookup"><span data-stu-id="773d5-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="773d5-112">Эта константа используется членом Вхкллевел <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="773d5-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="773d5-113">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="773d5-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="773d5-114">D3DENUM_WHQL_LEVEL не рекомендуется использовать для Direct3D9Ex, работающих под управлением Windows Vista, Windows Server 2008, Windows 7 и Windows Server 2008 R2 (или более текущей операционной системы).</span><span class="sxs-lookup"><span data-stu-id="773d5-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="773d5-115">Любая из этих операционных систем возвращает 1 для уровня WHQL без проверки состояния драйвера.</span><span class="sxs-lookup"><span data-stu-id="773d5-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="773d5-116">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="773d5-116">Constant Information</span></span>



| <span data-ttu-id="773d5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="773d5-117">Requirement</span></span>                         | <span data-ttu-id="773d5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="773d5-118">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="773d5-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="773d5-119">Header</span></span>                   | <span data-ttu-id="773d5-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="773d5-120">d3d9.h</span></span>     |
| <span data-ttu-id="773d5-121">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="773d5-121">Minimum operating system</span></span> | <span data-ttu-id="773d5-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="773d5-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="773d5-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="773d5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773d5-124">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="773d5-124">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




