---
title: Структура XMINT2
description: Описывает двухмерный целочисленный вектор.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- HLSL структура XMINT2
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222862"
---
# <a name="xmint2-structure"></a><span data-ttu-id="3b9b6-104">Структура XMINT2</span><span class="sxs-lookup"><span data-stu-id="3b9b6-104">XMINT2 structure</span></span>

<span data-ttu-id="3b9b6-105">Описывает двухмерный целочисленный вектор.</span><span class="sxs-lookup"><span data-stu-id="3b9b6-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9b6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b9b6-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="3b9b6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3b9b6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b9b6-108">**x**</span><span class="sxs-lookup"><span data-stu-id="3b9b6-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="3b9b6-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="3b9b6-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="3b9b6-110">**y**</span><span class="sxs-lookup"><span data-stu-id="3b9b6-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="3b9b6-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="3b9b6-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="3b9b6-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b9b6-112">Remarks</span></span>

<span data-ttu-id="3b9b6-113">Эта структура определена в ``D3DX\_DXGIFormatConvert.inl`` заголовке пакета SDK DirectX (июнь 2010) для использования из C++.</span><span class="sxs-lookup"><span data-stu-id="3b9b6-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="3b9b6-114">Последняя версия этого заголовка в пакете NuGet [Microsoft. дкссдк. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) больше не определяет его и использует [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) в директксмас.</span><span class="sxs-lookup"><span data-stu-id="3b9b6-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="3b9b6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3b9b6-115">Requirements</span></span>



| <span data-ttu-id="3b9b6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3b9b6-116">Requirement</span></span> | <span data-ttu-id="3b9b6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3b9b6-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9b6-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b9b6-118">Header</span></span><br/> | <dl> <span data-ttu-id="3b9b6-119"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="3b9b6-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9b6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b9b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9b6-121">Структуры</span><span class="sxs-lookup"><span data-stu-id="3b9b6-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="3b9b6-122">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="3b9b6-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
