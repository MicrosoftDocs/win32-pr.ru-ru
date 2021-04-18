---
description: Описывает разрешение теневого буфера z, которое будет использоваться в моделировании предварительно вычисленных Радианце (PRT) с прямым освещением на GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Перечисление D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713900"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="a3485-103">Перечисление D3DXSHGPUSIMOPT</span><span class="sxs-lookup"><span data-stu-id="a3485-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="a3485-104">Описывает разрешение теневого буфера z, которое будет использоваться в моделировании предварительно вычисленных Радианце (PRT) с прямым освещением на GPU.</span><span class="sxs-lookup"><span data-stu-id="a3485-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="a3485-105">Можно также задать z-буфер более высокого качества, чтобы уменьшить шум в результатах имитации прямого освещения, хотя моделирование будет выполняться медленнее.</span><span class="sxs-lookup"><span data-stu-id="a3485-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3485-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3485-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="a3485-107">Константы</span><span class="sxs-lookup"><span data-stu-id="a3485-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a3485-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**</span><span class="sxs-lookup"><span data-stu-id="a3485-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="a3485-109">Эмуляция с низким разрешением.</span><span class="sxs-lookup"><span data-stu-id="a3485-109">Low resolution simulation.</span></span> <span data-ttu-id="a3485-110">В моделировании используется текстура 256 x 256 пикселей для кодирования теневого z-буфера.</span><span class="sxs-lookup"><span data-stu-id="a3485-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a3485-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**</span><span class="sxs-lookup"><span data-stu-id="a3485-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="a3485-112">Эмуляция среднего разрешения.</span><span class="sxs-lookup"><span data-stu-id="a3485-112">Medium resolution simulation.</span></span> <span data-ttu-id="a3485-113">В моделировании используется текстура 512 x 512 пикселей для кодирования теневого z-буфера.</span><span class="sxs-lookup"><span data-stu-id="a3485-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="a3485-114">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3485-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="a3485-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**</span><span class="sxs-lookup"><span data-stu-id="a3485-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="a3485-116">Имитация высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="a3485-116">High resolution simulation.</span></span> <span data-ttu-id="a3485-117">В моделировании используется текстура 1024 x 1024 пикселей для кодирования теневого z-буфера.</span><span class="sxs-lookup"><span data-stu-id="a3485-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a3485-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**</span><span class="sxs-lookup"><span data-stu-id="a3485-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="a3485-119">Эмуляция наивысшего разрешения.</span><span class="sxs-lookup"><span data-stu-id="a3485-119">Highest resolution simulation.</span></span> <span data-ttu-id="a3485-120">В моделировании используется текстура 2048 x 2048 пикселей для кодирования теневого z-буфера.</span><span class="sxs-lookup"><span data-stu-id="a3485-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a3485-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ хигхкуалити**</span><span class="sxs-lookup"><span data-stu-id="a3485-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="a3485-122">Модель имеет высокую точность, независимо от выбранного разрешения.</span><span class="sxs-lookup"><span data-stu-id="a3485-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="a3485-123">Установка этого значения приведет к уменьшению шума в результатах имитации прямого освещения, хотя моделирование будет выполняться медленнее.</span><span class="sxs-lookup"><span data-stu-id="a3485-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="a3485-124">Может сочетаться с одним из значений разрешения.</span><span class="sxs-lookup"><span data-stu-id="a3485-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="a3485-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a3485-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a3485-126">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="a3485-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a3485-127">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="a3485-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a3485-128">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="a3485-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3485-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3485-129">Remarks</span></span>

<span data-ttu-id="a3485-130">Можно указать только одно из значений разрешения, и оно может сочетаться со значением высокого качества.</span><span class="sxs-lookup"><span data-stu-id="a3485-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3485-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a3485-131">Requirements</span></span>



| <span data-ttu-id="a3485-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a3485-132">Requirement</span></span> | <span data-ttu-id="a3485-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a3485-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3485-134">Header</span><span class="sxs-lookup"><span data-stu-id="a3485-134">Header</span></span><br/> | <dl> <span data-ttu-id="a3485-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3485-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3485-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3485-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3485-137">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="a3485-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




