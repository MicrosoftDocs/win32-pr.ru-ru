---
description: Оптимизирует сетку исправлений для эффективной тесселяции.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Метод ID3DXPatchMesh:: optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000526"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="1d999-103">Метод ID3DXPatchMesh:: OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="1d999-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="1d999-104">Оптимизирует сетку исправлений для эффективной тесселяции.</span><span class="sxs-lookup"><span data-stu-id="1d999-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d999-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d999-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="1d999-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d999-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d999-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1d999-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d999-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d999-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d999-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="1d999-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d999-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d999-110">Return value</span></span>

<span data-ttu-id="1d999-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d999-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d999-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1d999-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1d999-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ каннотаттрсорт.</span><span class="sxs-lookup"><span data-stu-id="1d999-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d999-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d999-114">Remarks</span></span>

<span data-ttu-id="1d999-115">После того как приложение создаст сведения о смежности для сетки, данные сетки могут быть оптимизированы (переупорядочены) для повышения производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="1d999-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="1d999-116">Этот метод определяет, какие исправления являются смежными (в пределах указанного допуска).</span><span class="sxs-lookup"><span data-stu-id="1d999-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="1d999-117">Для оптимизации тесселяции также используется соседеская информация.</span><span class="sxs-lookup"><span data-stu-id="1d999-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="1d999-118">Однократное создание сведений о смежности и формирование мозаики путем вызова [**ID3DXPatchMesh:: тесселяции**](id3dxpatchmesh--tessellate.md).</span><span class="sxs-lookup"><span data-stu-id="1d999-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="1d999-119">Выполняемая оптимизация не зависит от фактического используемого уровня тесселяции.</span><span class="sxs-lookup"><span data-stu-id="1d999-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="1d999-120">Однако при изменении вершин сетки необходимо повторно создать сведения о соседических данных.</span><span class="sxs-lookup"><span data-stu-id="1d999-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d999-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1d999-121">Requirements</span></span>



| <span data-ttu-id="1d999-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1d999-122">Requirement</span></span> | <span data-ttu-id="1d999-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1d999-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d999-124">Header</span><span class="sxs-lookup"><span data-stu-id="1d999-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d999-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d999-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1d999-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d999-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d999-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d999-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d999-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d999-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d999-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="1d999-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="1d999-130">**ID3DXPatchMesh:: Женератеаджаценци**</span><span class="sxs-lookup"><span data-stu-id="1d999-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
