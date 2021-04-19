---
title: Структура XMUINT2
description: Описывает двумерный вектор целых чисел без знака.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- HLSL структура XMUINT2
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ec040a848b3103b4d5070541f025ab9cfb0cfa
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222832"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="a04cc-104">Структура XMUINT2</span><span class="sxs-lookup"><span data-stu-id="a04cc-104">XMUINT2 structure</span></span>

<span data-ttu-id="a04cc-105">Описывает двумерный вектор целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="a04cc-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04cc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a04cc-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="a04cc-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a04cc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a04cc-108">**x**</span><span class="sxs-lookup"><span data-stu-id="a04cc-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="a04cc-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="a04cc-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="a04cc-110">**y**</span><span class="sxs-lookup"><span data-stu-id="a04cc-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="a04cc-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="a04cc-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="a04cc-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a04cc-112">Remarks</span></span>

<span data-ttu-id="a04cc-113">Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++.</span><span class="sxs-lookup"><span data-stu-id="a04cc-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="a04cc-114">Последняя версия этого заголовка в пакете NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) больше не определяет его и использует [DirectX:: XMUINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint2) в директксмас.</span><span class="sxs-lookup"><span data-stu-id="a04cc-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="a04cc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a04cc-115">Requirements</span></span>



| <span data-ttu-id="a04cc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a04cc-116">Requirement</span></span> | <span data-ttu-id="a04cc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a04cc-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a04cc-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a04cc-118">Header</span></span><br/> | <dl> <span data-ttu-id="a04cc-119"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="a04cc-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04cc-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a04cc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04cc-121">Структуры</span><span class="sxs-lookup"><span data-stu-id="a04cc-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="a04cc-122">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="a04cc-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
