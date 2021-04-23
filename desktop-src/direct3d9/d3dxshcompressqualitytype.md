---
description: Параметр энергосферовой гармонии (SH).
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: Перечисление D3DXSHCOMPRESSQUALITYTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d61c70317505442ca4911a13dac8566f9bd7c6fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273759"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a><span data-ttu-id="8deb5-103">Перечисление D3DXSHCOMPRESSQUALITYTYPE</span><span class="sxs-lookup"><span data-stu-id="8deb5-103">D3DXSHCOMPRESSQUALITYTYPE enumeration</span></span>

<span data-ttu-id="8deb5-104">Параметр энергосферовой гармонии (SH).</span><span class="sxs-lookup"><span data-stu-id="8deb5-104">Spherical harmonic (SH) compression setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="8deb5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8deb5-105">Syntax</span></span>


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a><span data-ttu-id="8deb5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="8deb5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8deb5-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL \_ фастловкуалити**</span><span class="sxs-lookup"><span data-stu-id="8deb5-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL\_FASTLOWQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="8deb5-108">Сжатие данных имеет низкий уровень качества, но ускоряет сжатие.</span><span class="sxs-lookup"><span data-stu-id="8deb5-108">The data compression is low quality, but is fast to compress.</span></span>

</dd> <dt>

<span data-ttu-id="8deb5-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL \_ словхигхкуалити**</span><span class="sxs-lookup"><span data-stu-id="8deb5-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL\_SLOWHIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="8deb5-110">Сжатие данных имеет высокое качество, но сжимается слишком долго.</span><span class="sxs-lookup"><span data-stu-id="8deb5-110">The data compression is high quality, but is slow to compress.</span></span>

</dd> <dt>

<span data-ttu-id="8deb5-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8deb5-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8deb5-112">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="8deb5-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8deb5-113">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="8deb5-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8deb5-114">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="8deb5-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8deb5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8deb5-115">Requirements</span></span>



| <span data-ttu-id="8deb5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8deb5-116">Requirement</span></span> | <span data-ttu-id="8deb5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8deb5-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8deb5-118">Header</span><span class="sxs-lookup"><span data-stu-id="8deb5-118">Header</span></span><br/> | <dl> <span data-ttu-id="8deb5-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8deb5-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8deb5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8deb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8deb5-121">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="8deb5-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




