---
description: Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'Метод ID3DXMesh:: Сетаттрибутетабле (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703690"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="f229c-103">Метод ID3DXMesh:: Сетаттрибутетабле</span><span class="sxs-lookup"><span data-stu-id="f229c-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="f229c-104">Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.</span><span class="sxs-lookup"><span data-stu-id="f229c-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="f229c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f229c-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="f229c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f229c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f229c-107">*паттрибтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f229c-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f229c-108">Тип: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="f229c-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="f229c-109">Указатель на массив структур [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , представляющий записи в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="f229c-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="f229c-110">*каттрибтаблесизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f229c-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f229c-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f229c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f229c-112">Число атрибутов в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="f229c-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f229c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f229c-113">Return value</span></span>

<span data-ttu-id="f229c-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f229c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f229c-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f229c-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f229c-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f229c-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f229c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f229c-117">Remarks</span></span>

<span data-ttu-id="f229c-118">Если приложение отслеживает сведения в таблице атрибутов и переупорядочивает таблицу в результате изменений атрибутов или лиц, этот метод позволяет приложению обновлять таблицы атрибутов вместо вызова [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="f229c-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="f229c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f229c-119">Requirements</span></span>



| <span data-ttu-id="f229c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f229c-120">Requirement</span></span> | <span data-ttu-id="f229c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f229c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f229c-122">Header</span><span class="sxs-lookup"><span data-stu-id="f229c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f229c-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f229c-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f229c-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f229c-124">Library</span></span><br/> | <dl> <span data-ttu-id="f229c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f229c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f229c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f229c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f229c-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="f229c-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="f229c-128">**ID3DXMesh:: Локкаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="f229c-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="f229c-129">**ID3DXMesh:: Локкаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="f229c-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
