---
description: Описывает режим экрана.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: Структура D3DDISPLAYMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157155"
---
# <a name="d3ddisplaymode-structure"></a><span data-ttu-id="b0d2c-103">Структура D3DDISPLAYMODE</span><span class="sxs-lookup"><span data-stu-id="b0d2c-103">D3DDISPLAYMODE structure</span></span>

<span data-ttu-id="b0d2c-104">Описывает режим экрана.</span><span class="sxs-lookup"><span data-stu-id="b0d2c-104">Describes the display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0d2c-105">Syntax</span></span>


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a><span data-ttu-id="b0d2c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b0d2c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0d2c-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b0d2c-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0d2c-109">Ширина экрана (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="b0d2c-109">Screen width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b0d2c-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b0d2c-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0d2c-112">Высота экрана (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="b0d2c-112">Screen height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b0d2c-113">**рефрешрате**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-113">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="b0d2c-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0d2c-115">Частота обновления.</span><span class="sxs-lookup"><span data-stu-id="b0d2c-115">Refresh rate.</span></span> <span data-ttu-id="b0d2c-116">Значение 0 указывает на адаптер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b0d2c-116">The value of 0 indicates an adapter default.</span></span>

</dd> <dt>

<span data-ttu-id="b0d2c-117">**Формат**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-117">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="b0d2c-118">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b0d2c-119">Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности режима отображения.</span><span class="sxs-lookup"><span data-stu-id="b0d2c-119">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the display mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0d2c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b0d2c-120">Requirements</span></span>



| <span data-ttu-id="b0d2c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b0d2c-121">Requirement</span></span> | <span data-ttu-id="b0d2c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b0d2c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d2c-123">Header</span><span class="sxs-lookup"><span data-stu-id="b0d2c-123">Header</span></span><br/> | <dl> <span data-ttu-id="b0d2c-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d2c-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d2c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0d2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d2c-126">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="b0d2c-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b0d2c-127">**енумадаптермодес**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-127">**EnumAdapterModes**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[<span data-ttu-id="b0d2c-128">**жетадаптердисплаймоде**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-128">**GetAdapterDisplayMode**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[<span data-ttu-id="b0d2c-129">**жетдисплаймоде**</span><span class="sxs-lookup"><span data-stu-id="b0d2c-129">**GetDisplayMode**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
