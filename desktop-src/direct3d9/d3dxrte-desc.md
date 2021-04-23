---
description: Описывает экранный целевой объект отрисовки, используемый экземпляром ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Структура D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273765"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="c0bbc-103">\_Структура D3DXRTE DESC</span><span class="sxs-lookup"><span data-stu-id="c0bbc-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="c0bbc-104">Описывает экранный целевой объект отрисовки, используемый экземпляром [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span><span class="sxs-lookup"><span data-stu-id="c0bbc-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0bbc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0bbc-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="c0bbc-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c0bbc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0bbc-107">**Размер**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="c0bbc-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0bbc-109">Ширина и высота в пикселях.</span><span class="sxs-lookup"><span data-stu-id="c0bbc-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c0bbc-110">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="c0bbc-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0bbc-112">Максимальный уровень детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="c0bbc-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="c0bbc-113">**Формат**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="c0bbc-114">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0bbc-115">Формат цветового буфера.</span><span class="sxs-lookup"><span data-stu-id="c0bbc-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="c0bbc-116">**депсстенЦил**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="c0bbc-117">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0bbc-118">Указывает, требуется ли z-буфер.</span><span class="sxs-lookup"><span data-stu-id="c0bbc-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="c0bbc-119">**депсстенЦилформат**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="c0bbc-120">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c0bbc-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c0bbc-121">Формат буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="c0bbc-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0bbc-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0bbc-122">Remarks</span></span>

<span data-ttu-id="c0bbc-123">Этот метод используется для возврата параметров создания, используемых при создании объекта [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="c0bbc-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0bbc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c0bbc-124">Requirements</span></span>



| <span data-ttu-id="c0bbc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c0bbc-125">Requirement</span></span> | <span data-ttu-id="c0bbc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c0bbc-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0bbc-127">Header</span><span class="sxs-lookup"><span data-stu-id="c0bbc-127">Header</span></span><br/> | <dl> <span data-ttu-id="c0bbc-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0bbc-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0bbc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0bbc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0bbc-130">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="c0bbc-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
