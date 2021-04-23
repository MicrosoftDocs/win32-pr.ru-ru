---
title: Структура XMUINT4
description: Описывает вектор целого числа без знака 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- HLSL структура XMUINT4
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222852"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="fe123-104">Структура XMUINT4</span><span class="sxs-lookup"><span data-stu-id="fe123-104">XMUINT4 structure</span></span>

<span data-ttu-id="fe123-105">Описывает вектор целого числа без знака 4D.</span><span class="sxs-lookup"><span data-stu-id="fe123-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe123-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe123-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="fe123-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fe123-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe123-108">**x**</span><span class="sxs-lookup"><span data-stu-id="fe123-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="fe123-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="fe123-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="fe123-110">**y**</span><span class="sxs-lookup"><span data-stu-id="fe123-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="fe123-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="fe123-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="fe123-112">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="fe123-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="fe123-113">z-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="fe123-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="fe123-114">**w**</span><span class="sxs-lookup"><span data-stu-id="fe123-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="fe123-115">w — компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="fe123-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="fe123-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe123-116">Remarks</span></span>

<span data-ttu-id="fe123-117">Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++.</span><span class="sxs-lookup"><span data-stu-id="fe123-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="fe123-118">Последняя версия этого заголовка в пакете NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) больше не определяет его и использует [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) в директксмас.</span><span class="sxs-lookup"><span data-stu-id="fe123-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="fe123-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fe123-119">Requirements</span></span>



| <span data-ttu-id="fe123-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fe123-120">Requirement</span></span> | <span data-ttu-id="fe123-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fe123-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe123-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fe123-122">Header</span></span><br/> | <dl> <span data-ttu-id="fe123-123"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fe123-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe123-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe123-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe123-125">Структуры</span><span class="sxs-lookup"><span data-stu-id="fe123-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="fe123-126">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="fe123-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
