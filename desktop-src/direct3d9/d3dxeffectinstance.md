---
description: Тип данных для управления набором параметров эффектов по умолчанию.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Структура D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354883"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="ef074-103">Структура D3DXEFFECTINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef074-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="ef074-104">Тип данных для управления набором параметров эффектов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef074-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef074-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef074-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="ef074-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ef074-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef074-107">**пеффектфиленаме**</span><span class="sxs-lookup"><span data-stu-id="ef074-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="ef074-108">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="ef074-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ef074-109">Имя файла действия.</span><span class="sxs-lookup"><span data-stu-id="ef074-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="ef074-110">**нумдефаултс**</span><span class="sxs-lookup"><span data-stu-id="ef074-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="ef074-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef074-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef074-112">Количество параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef074-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="ef074-113">**пдефаултс**</span><span class="sxs-lookup"><span data-stu-id="ef074-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="ef074-114">Тип: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="ef074-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef074-115">Указатель на массив элементов [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , каждый из которых содержит параметр Effect.</span><span class="sxs-lookup"><span data-stu-id="ef074-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef074-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ef074-116">Requirements</span></span>



| <span data-ttu-id="ef074-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ef074-117">Requirement</span></span> | <span data-ttu-id="ef074-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ef074-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef074-119">Header</span><span class="sxs-lookup"><span data-stu-id="ef074-119">Header</span></span><br/> | <dl> <span data-ttu-id="ef074-120"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef074-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef074-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef074-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef074-122">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="ef074-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
