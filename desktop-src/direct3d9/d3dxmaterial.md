---
description: Возвращает сведения о материалах, сохраненные в файлах Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Структура D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703647"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="1a20a-103">Структура D3DXMATERIAL</span><span class="sxs-lookup"><span data-stu-id="1a20a-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="1a20a-104">Возвращает сведения о материалах, сохраненные в файлах Direct3D (. x).</span><span class="sxs-lookup"><span data-stu-id="1a20a-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a20a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a20a-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="1a20a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1a20a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1a20a-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="1a20a-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="1a20a-108">Тип: **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="1a20a-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1a20a-109">Структура [**D3DMATERIAL9**](d3dmaterial9.md) , описывающая свойства материала.</span><span class="sxs-lookup"><span data-stu-id="1a20a-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="1a20a-110">**птекстурефиленаме**</span><span class="sxs-lookup"><span data-stu-id="1a20a-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="1a20a-111">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="1a20a-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="1a20a-112">Указатель на строку, указывающую имя файла текстуры.</span><span class="sxs-lookup"><span data-stu-id="1a20a-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a20a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a20a-113">Remarks</span></span>

<span data-ttu-id="1a20a-114">Функции [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) и [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) возвращают массив структур **D3DXMATERIAL** , которые определяют цвет материала и название текстуры для каждого материала в сети.</span><span class="sxs-lookup"><span data-stu-id="1a20a-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="1a20a-115">Затем приложение требуется для загрузки текстуры.</span><span class="sxs-lookup"><span data-stu-id="1a20a-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="1a20a-116">Тип LPD3DXMATERIAL определяется как указатель на структуру **D3DXMATERIAL** .</span><span class="sxs-lookup"><span data-stu-id="1a20a-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="1a20a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1a20a-117">Requirements</span></span>



| <span data-ttu-id="1a20a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1a20a-118">Requirement</span></span> | <span data-ttu-id="1a20a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1a20a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a20a-120">Header</span><span class="sxs-lookup"><span data-stu-id="1a20a-120">Header</span></span><br/> | <dl> <span data-ttu-id="1a20a-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a20a-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a20a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a20a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a20a-123">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="1a20a-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="1a20a-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="1a20a-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="1a20a-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="1a20a-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




