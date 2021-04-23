---
description: Описывает Заблокированную прямоугольную область.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Структура D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547967"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="9d747-103">\_Структура Rect D3DLOCKED</span><span class="sxs-lookup"><span data-stu-id="9d747-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="9d747-104">Описывает Заблокированную прямоугольную область.</span><span class="sxs-lookup"><span data-stu-id="9d747-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d747-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d747-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="9d747-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9d747-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d747-107">**Высота тона**</span><span class="sxs-lookup"><span data-stu-id="9d747-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="9d747-108">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d747-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d747-109">Число байтов в одной строке поверхности.</span><span class="sxs-lookup"><span data-stu-id="9d747-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="9d747-110">**пбитс**</span><span class="sxs-lookup"><span data-stu-id="9d747-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="9d747-111">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="9d747-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="9d747-112">Указатель на заблокированные биты.</span><span class="sxs-lookup"><span data-stu-id="9d747-112">Pointer to the locked bits.</span></span> <span data-ttu-id="9d747-113">Если для вызова [**локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) был предоставлен [**Rect**](/previous-versions//dd162897(v=vs.85)) , пбитс будет соответствующим образом смещен с начала поверхности.</span><span class="sxs-lookup"><span data-stu-id="9d747-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d747-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d747-114">Remarks</span></span>

<span data-ttu-id="9d747-115">Высота форматов Дкстн отличается от того, что было возвращено в DirectX 7.</span><span class="sxs-lookup"><span data-stu-id="9d747-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="9d747-116">Теперь он ссылается на число байтов в строке блоков.</span><span class="sxs-lookup"><span data-stu-id="9d747-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="9d747-117">Например, если ширина 16, то у вас будет шаг 4 блока (4 \* 8 для DXT1, 4 \* 16 для DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="9d747-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="9d747-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9d747-118">Requirements</span></span>



| <span data-ttu-id="9d747-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9d747-119">Requirement</span></span> | <span data-ttu-id="9d747-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9d747-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d747-121">Header</span><span class="sxs-lookup"><span data-stu-id="9d747-121">Header</span></span><br/> | <dl> <span data-ttu-id="9d747-122"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d747-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d747-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d747-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d747-124">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9d747-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9d747-125">**IDirect3DCubeTexture9:: Локкрект**</span><span class="sxs-lookup"><span data-stu-id="9d747-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="9d747-126">**IDirect3DSurface9:: Локкрект**</span><span class="sxs-lookup"><span data-stu-id="9d747-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="9d747-127">**IDirect3DTexture9:: Локкрект**</span><span class="sxs-lookup"><span data-stu-id="9d747-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
