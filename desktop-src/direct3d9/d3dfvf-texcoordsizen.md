---
description: Конструирует битовые шаблоны, используемые для распознавания форматов координат текстуры в описании ФВФ. Результаты этих макросов можно объединить в описании ФВФ с помощью оператора или.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703846"
---
# <a name="d3dfvf_texcoordsizen"></a><span data-ttu-id="68486-104">D3DFVF \_ текскурдсизен</span><span class="sxs-lookup"><span data-stu-id="68486-104">D3DFVF\_TEXCOORDSIZEN</span></span>

<span data-ttu-id="68486-105">Конструирует битовые шаблоны, используемые для распознавания форматов координат текстуры в описании ФВФ.</span><span class="sxs-lookup"><span data-stu-id="68486-105">Constructs bit patterns that are used to identify texture coordinate formats within a FVF description.</span></span> <span data-ttu-id="68486-106">Результаты этих макросов можно объединить в описании ФВФ с помощью оператора или.</span><span class="sxs-lookup"><span data-stu-id="68486-106">The results of these macros can be combined within a FVF description by using the OR operator.</span></span>

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a><span data-ttu-id="68486-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="68486-107">Parameters</span></span>



| <span data-ttu-id="68486-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="68486-108">Parameter</span></span>                                                                                                    | <span data-ttu-id="68486-109">Описание</span><span class="sxs-lookup"><span data-stu-id="68486-109">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68486-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>курдиндекс</span><span class="sxs-lookup"><span data-stu-id="68486-110"><span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex</span></span><br/> | <span data-ttu-id="68486-111">Значение, определяющее набор координат текстуры, в котором применяется размер координаты текстуры (1-, 2-, 3-или 4Dimensional).</span><span class="sxs-lookup"><span data-stu-id="68486-111">Value that identifies the texture coordinate set at which the texture coordinate size (1-, 2-, 3-, or 4Dimensional) applies.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="68486-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68486-112">Remarks</span></span>

<span data-ttu-id="68486-113">Макросы **\_ текскурдсизен D3DFVF** используют следующие константы.</span><span class="sxs-lookup"><span data-stu-id="68486-113">The **D3DFVF\_TEXCOORDSIZEN** macros use the following constants.</span></span>


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



<span data-ttu-id="68486-114">Следующее описание ФВФ определяет формат вершины, в котором есть расположение. Обычная; рассеянные и бликовые цвета; и два набора координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="68486-114">The following FVF description identifies a vertex format that has a position; a normal; diffuse and specular colors; and two sets of texture coordinates.</span></span> <span data-ttu-id="68486-115">Первый набор координат текстуры включает один элемент, а второй набор включает два элемента:</span><span class="sxs-lookup"><span data-stu-id="68486-115">The first set of texture coordinates includes a single element, and the second set includes two elements:</span></span>


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a><span data-ttu-id="68486-116">Требования</span><span class="sxs-lookup"><span data-stu-id="68486-116">Requirements</span></span>



| <span data-ttu-id="68486-117">Требование</span><span class="sxs-lookup"><span data-stu-id="68486-117">Requirement</span></span> | <span data-ttu-id="68486-118">Значение</span><span class="sxs-lookup"><span data-stu-id="68486-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68486-119">Header</span><span class="sxs-lookup"><span data-stu-id="68486-119">Header</span></span><br/> | <dl> <span data-ttu-id="68486-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="68486-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68486-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68486-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68486-122">Макросы</span><span class="sxs-lookup"><span data-stu-id="68486-122">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="68486-123">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="68486-123">D3DFVF</span></span>](d3dfvf.md)
</dt> </dl>

 

 




