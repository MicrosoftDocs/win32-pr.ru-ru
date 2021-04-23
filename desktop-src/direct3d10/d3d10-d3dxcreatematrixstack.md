---
description: Создание стека матриц.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Функция D3DXCreateMatrixStack (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424473"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="79f38-103">Функция D3DXCreateMatrixStack (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="79f38-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="79f38-104">Создание стека матриц.</span><span class="sxs-lookup"><span data-stu-id="79f38-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79f38-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="79f38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79f38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f38-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79f38-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f38-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79f38-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79f38-109">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="79f38-109">Not implemented.</span></span> <span data-ttu-id="79f38-110">Укажите нуль.</span><span class="sxs-lookup"><span data-stu-id="79f38-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="79f38-111">*ппстакк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79f38-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79f38-112">Тип: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="79f38-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="79f38-113">Адрес указателя на стек матрицы (см. [**интерфейс ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).</span><span class="sxs-lookup"><span data-stu-id="79f38-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f38-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79f38-114">Return value</span></span>

<span data-ttu-id="79f38-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79f38-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79f38-116">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="79f38-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79f38-117">Требования</span><span class="sxs-lookup"><span data-stu-id="79f38-117">Requirements</span></span>



| <span data-ttu-id="79f38-118">Требование</span><span class="sxs-lookup"><span data-stu-id="79f38-118">Requirement</span></span> | <span data-ttu-id="79f38-119">Значение</span><span class="sxs-lookup"><span data-stu-id="79f38-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79f38-120">Header</span><span class="sxs-lookup"><span data-stu-id="79f38-120">Header</span></span><br/>  | <dl> <span data-ttu-id="79f38-121"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f38-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="79f38-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79f38-122">Library</span></span><br/> | <dl> <span data-ttu-id="79f38-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79f38-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="79f38-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79f38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f38-125">Математические функции</span><span class="sxs-lookup"><span data-stu-id="79f38-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
