---
description: Извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'Метод ID3DX10Mesh:: Жетаттрибутетабле (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703894"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="ba7df-103">Метод ID3DX10Mesh:: Жетаттрибутетабле</span><span class="sxs-lookup"><span data-stu-id="ba7df-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="ba7df-104">Извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="ba7df-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba7df-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="ba7df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba7df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba7df-107">*паттрибтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba7df-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7df-108">Тип: **[ **D3DX10 \_ \_ диапазон атрибутов**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba7df-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="ba7df-109">Указатель на массив \_ структур диапазона АТРИБУТОВ D3DX10 \_ , представляющий записи в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="ba7df-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="ba7df-110">Чтобы получить значение для Паттрибтаблесизе, укажите значение **null** .</span><span class="sxs-lookup"><span data-stu-id="ba7df-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="ba7df-111">*паттрибтаблесизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba7df-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7df-112">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba7df-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ba7df-113">Указатель на количество записей, хранящихся в Паттрибтабле, или значение, которое должно быть заполнено количеством записей, хранящихся в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="ba7df-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba7df-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba7df-114">Return value</span></span>

<span data-ttu-id="ba7df-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba7df-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba7df-116">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ba7df-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba7df-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba7df-117">Remarks</span></span>

<span data-ttu-id="ba7df-118">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="ba7df-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="ba7df-119">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="ba7df-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7df-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ba7df-120">Requirements</span></span>



| <span data-ttu-id="ba7df-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ba7df-121">Requirement</span></span> | <span data-ttu-id="ba7df-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ba7df-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7df-123">Header</span><span class="sxs-lookup"><span data-stu-id="ba7df-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ba7df-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba7df-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba7df-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba7df-125">Library</span></span><br/> | <dl> <span data-ttu-id="ba7df-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba7df-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba7df-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba7df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7df-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ba7df-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ba7df-129">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ba7df-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
