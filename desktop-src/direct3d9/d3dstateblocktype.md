---
description: Предопределенные наборы состояний конвейера, используемые блоками состояния (см. раздел State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Перечисление D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104550571"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="1cf80-103">Перечисление D3DSTATEBLOCKTYPE</span><span class="sxs-lookup"><span data-stu-id="1cf80-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="1cf80-104">Предопределенные наборы состояний конвейера, используемые блоками состояния (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="1cf80-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cf80-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="1cf80-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1cf80-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1cf80-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ все**</span><span class="sxs-lookup"><span data-stu-id="1cf80-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="1cf80-108">Запись текущего [состояния устройства](saving-all-device-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="1cf80-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf80-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ пикселстате**</span><span class="sxs-lookup"><span data-stu-id="1cf80-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="1cf80-110">Захватывает текущее [состояние пикселя](saving-pixel-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="1cf80-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf80-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ вертексстате**</span><span class="sxs-lookup"><span data-stu-id="1cf80-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="1cf80-112">Захватывает текущее [состояние вершины](saving-vertex-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="1cf80-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf80-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1cf80-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1cf80-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="1cf80-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1cf80-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="1cf80-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1cf80-116">Не используйте это значение.</span><span class="sxs-lookup"><span data-stu-id="1cf80-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cf80-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cf80-117">Remarks</span></span>

<span data-ttu-id="1cf80-118">Как показано на следующей схеме, состояние вершины и пиксела — это оба подмножества состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="1cf80-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![Схема состояния устройства с состоянием вершины и состоянием пикселя в качестве подмножества](images/statesets.png)

<span data-ttu-id="1cf80-120">Существует только несколько состояний, которые считаются состоянием вершины и пикселя.</span><span class="sxs-lookup"><span data-stu-id="1cf80-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="1cf80-121">Возможны следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="1cf80-121">These states are:</span></span>

-   <span data-ttu-id="1cf80-122">Состояние визуализации: D3DRS \_ фогденсити</span><span class="sxs-lookup"><span data-stu-id="1cf80-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="1cf80-123">Состояние визуализации: D3DRS \_ фогстарт</span><span class="sxs-lookup"><span data-stu-id="1cf80-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="1cf80-124">Состояние визуализации: D3DRS \_ фоженд</span><span class="sxs-lookup"><span data-stu-id="1cf80-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="1cf80-125">Состояние текстуры: D3DTSS \_ текскурдиндекс</span><span class="sxs-lookup"><span data-stu-id="1cf80-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="1cf80-126">Состояние текстуры: D3DTSS \_ текстуретрансформфлагс</span><span class="sxs-lookup"><span data-stu-id="1cf80-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf80-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1cf80-127">Requirements</span></span>



| <span data-ttu-id="1cf80-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1cf80-128">Requirement</span></span> | <span data-ttu-id="1cf80-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1cf80-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf80-130">Header</span><span class="sxs-lookup"><span data-stu-id="1cf80-130">Header</span></span><br/> | <dl> <span data-ttu-id="1cf80-131"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf80-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf80-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cf80-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf80-133">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="1cf80-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1cf80-134">**IDirect3DDevice9:: Креатестатеблокк**</span><span class="sxs-lookup"><span data-stu-id="1cf80-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="1cf80-135">**IDirect3DDevice9:: Креатестатеблокк**</span><span class="sxs-lookup"><span data-stu-id="1cf80-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
