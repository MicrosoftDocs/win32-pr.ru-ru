---
description: Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'Метод ID3DX10Mesh:: Сетаттрибутетабле (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273873"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="6d812-103">Метод ID3DX10Mesh:: Сетаттрибутетабле</span><span class="sxs-lookup"><span data-stu-id="6d812-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="6d812-104">Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.</span><span class="sxs-lookup"><span data-stu-id="6d812-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d812-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d812-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="6d812-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d812-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d812-107">*паттрибтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d812-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d812-108">Тип: **\* [**\_ \_ диапазон атрибутов const D3DX10**](d3dx10-attribute-range.md)**</span><span class="sxs-lookup"><span data-stu-id="6d812-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="6d812-109">Указатель на массив \_ структур диапазона АТРИБУТОВ D3DX10 \_ , представляющий записи в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="6d812-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="6d812-110">*каттрибтаблесизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d812-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d812-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d812-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d812-112">Число атрибутов в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="6d812-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d812-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d812-113">Return value</span></span>

<span data-ttu-id="6d812-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d812-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d812-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6d812-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d812-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d812-116">Remarks</span></span>

<span data-ttu-id="6d812-117">Если приложение отслеживает сведения в таблице атрибутов и переупорядочивает таблицу в результате изменений атрибутов или лиц, этот метод позволяет приложению обновлять таблицы атрибутов вместо вызова ID3DX10Mesh:: optimize.</span><span class="sxs-lookup"><span data-stu-id="6d812-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d812-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6d812-118">Requirements</span></span>



| <span data-ttu-id="6d812-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6d812-119">Requirement</span></span> | <span data-ttu-id="6d812-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6d812-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d812-121">Header</span><span class="sxs-lookup"><span data-stu-id="6d812-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6d812-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d812-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d812-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d812-123">Library</span></span><br/> | <dl> <span data-ttu-id="6d812-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d812-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d812-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d812-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d812-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="6d812-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="6d812-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="6d812-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
