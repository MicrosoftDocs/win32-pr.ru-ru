---
title: Структура XMINT4
description: Описывает целочисленный вектор 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL структура XMINT4
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549959"
---
# <a name="xmint4-structure"></a><span data-ttu-id="29e5e-104">Структура XMINT4</span><span class="sxs-lookup"><span data-stu-id="29e5e-104">XMINT4 structure</span></span>

<span data-ttu-id="29e5e-105">Описывает целочисленный вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="29e5e-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e5e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29e5e-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="29e5e-107">Участники</span><span class="sxs-lookup"><span data-stu-id="29e5e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="29e5e-108">**x**</span><span class="sxs-lookup"><span data-stu-id="29e5e-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="29e5e-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="29e5e-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="29e5e-110">**y**</span><span class="sxs-lookup"><span data-stu-id="29e5e-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="29e5e-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="29e5e-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="29e5e-112">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="29e5e-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="29e5e-113">z-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="29e5e-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="29e5e-114">**w**</span><span class="sxs-lookup"><span data-stu-id="29e5e-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="29e5e-115">w — компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="29e5e-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29e5e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="29e5e-116">Requirements</span></span>



| <span data-ttu-id="29e5e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="29e5e-117">Requirement</span></span> | <span data-ttu-id="29e5e-118">Применение</span><span class="sxs-lookup"><span data-stu-id="29e5e-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e5e-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29e5e-119">Header</span></span><br/> | <dl> <span data-ttu-id="29e5e-120"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="29e5e-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="29e5e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29e5e-121">Remarks</span></span>

<span data-ttu-id="29e5e-122">Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++.</span><span class="sxs-lookup"><span data-stu-id="29e5e-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="29e5e-123">Последняя версия этого заголовка в пакете NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) больше не определяет его и использует [DirectX:: XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) в директксмас.</span><span class="sxs-lookup"><span data-stu-id="29e5e-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="29e5e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="29e5e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e5e-125">Структуры</span><span class="sxs-lookup"><span data-stu-id="29e5e-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="29e5e-126">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="29e5e-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>