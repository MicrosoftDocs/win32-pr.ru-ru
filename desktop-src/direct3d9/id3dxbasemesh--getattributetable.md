---
description: 'Метод ID3DXBaseMesh:: Жетаттрибутетабле — извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'Метод ID3DXBaseMesh:: Жетаттрибутетабле (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115452"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="3620d-103">Метод ID3DXBaseMesh:: Жетаттрибутетабле</span><span class="sxs-lookup"><span data-stu-id="3620d-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="3620d-104">Извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="3620d-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3620d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3620d-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="3620d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3620d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3620d-107">*паттрибтабле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3620d-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3620d-108">Тип: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="3620d-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="3620d-109">Указатель на массив структур [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , представляющий записи в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="3620d-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="3620d-110">Чтобы получить значение для Паттрибтаблесизе, укажите значение **null** .</span><span class="sxs-lookup"><span data-stu-id="3620d-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="3620d-111">*паттрибтаблесизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3620d-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3620d-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3620d-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3620d-113">Указатель на количество записей, хранящихся в Паттрибтабле, или значение, которое должно быть заполнено количеством записей, хранящихся в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="3620d-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3620d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3620d-114">Return value</span></span>

<span data-ttu-id="3620d-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3620d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3620d-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3620d-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3620d-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="3620d-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3620d-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="3620d-118">Remarks</span></span>

<span data-ttu-id="3620d-119">Таблица атрибутов создается с помощью [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) и передает D3DXMESHOPT \_ Аттрсорт для параметра flags.</span><span class="sxs-lookup"><span data-stu-id="3620d-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="3620d-120">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="3620d-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="3620d-121">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="3620d-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="3620d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3620d-122">Requirements</span></span>



| <span data-ttu-id="3620d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3620d-123">Requirement</span></span> | <span data-ttu-id="3620d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3620d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3620d-125">Header</span><span class="sxs-lookup"><span data-stu-id="3620d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3620d-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3620d-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3620d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3620d-127">Library</span></span><br/> | <dl> <span data-ttu-id="3620d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3620d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3620d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3620d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3620d-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="3620d-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
