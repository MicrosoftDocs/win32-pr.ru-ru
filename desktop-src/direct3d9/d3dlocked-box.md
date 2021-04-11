---
description: Описывает заблокированный прямоугольник (том).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Структура D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273832"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="49b81-103">\_Структура Box D3DLOCKED</span><span class="sxs-lookup"><span data-stu-id="49b81-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="49b81-104">Описывает заблокированный прямоугольник (том).</span><span class="sxs-lookup"><span data-stu-id="49b81-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="49b81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49b81-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="49b81-106">Члены</span><span class="sxs-lookup"><span data-stu-id="49b81-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="49b81-107">**ровпитч**</span><span class="sxs-lookup"><span data-stu-id="49b81-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="49b81-108">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49b81-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49b81-109">Смещение в байтах от левого края одной строки к левому краю следующей строки.</span><span class="sxs-lookup"><span data-stu-id="49b81-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="49b81-110">**слицепитч**</span><span class="sxs-lookup"><span data-stu-id="49b81-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="49b81-111">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49b81-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="49b81-112">Смещение в байтах от верхнего левого угла одного среза к левому верхнему краю следующего самого глубокого среза.</span><span class="sxs-lookup"><span data-stu-id="49b81-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="49b81-113">**пбитс**</span><span class="sxs-lookup"><span data-stu-id="49b81-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="49b81-114">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="49b81-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="49b81-115">Указатель на начало поля "том".</span><span class="sxs-lookup"><span data-stu-id="49b81-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="49b81-116">Если в вызове защищенного хранилища была предоставлена [**D3DBOX**](d3dbox.md) , пбитс будет соответствующим образом смещен с начала тома.</span><span class="sxs-lookup"><span data-stu-id="49b81-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49b81-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49b81-117">Remarks</span></span>

<span data-ttu-id="49b81-118">Тома могут быть визуально обрабатываются в виде срезов 2D-поверхностей толщины x высота, разбитого на оси x высота x глубина.</span><span class="sxs-lookup"><span data-stu-id="49b81-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="49b81-119">Дополнительные сведения см. в статье [ресурсы текстуры для томов (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="49b81-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49b81-120">Требования</span><span class="sxs-lookup"><span data-stu-id="49b81-120">Requirements</span></span>



| <span data-ttu-id="49b81-121">Требование</span><span class="sxs-lookup"><span data-stu-id="49b81-121">Requirement</span></span> | <span data-ttu-id="49b81-122">Значение</span><span class="sxs-lookup"><span data-stu-id="49b81-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49b81-123">Header</span><span class="sxs-lookup"><span data-stu-id="49b81-123">Header</span></span><br/> | <dl> <span data-ttu-id="49b81-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="49b81-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b81-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49b81-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b81-126">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="49b81-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="49b81-127">**IDirect3DVolume9:: защищенное хранилище**</span><span class="sxs-lookup"><span data-stu-id="49b81-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="49b81-128">**IDirect3DVolumeTexture9:: защищенное хранилище**</span><span class="sxs-lookup"><span data-stu-id="49b81-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
