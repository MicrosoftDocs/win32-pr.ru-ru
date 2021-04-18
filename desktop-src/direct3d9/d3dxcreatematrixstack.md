---
description: Создает экземпляр интерфейса ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: Функция D3DXCreateMatrixStack (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694254"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="fd0bb-103">Функция D3DXCreateMatrixStack (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fd0bb-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="fd0bb-104">Создает экземпляр интерфейса [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="fd0bb-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd0bb-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="fd0bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd0bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd0bb-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd0bb-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0bb-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd0bb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd0bb-109">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="fd0bb-109">Not implemented.</span></span> <span data-ttu-id="fd0bb-110">Укажите нуль.</span><span class="sxs-lookup"><span data-stu-id="fd0bb-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd0bb-111">*ппстакк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fd0bb-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0bb-112">Тип: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="fd0bb-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="fd0bb-113">Адрес указателя, заполненного указателем интерфейса [**ID3DXMATRIXStack**](id3dxmatrixstack.md) , если функция выполнена.</span><span class="sxs-lookup"><span data-stu-id="fd0bb-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd0bb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd0bb-114">Return value</span></span>

<span data-ttu-id="fd0bb-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd0bb-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd0bb-116">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fd0bb-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fd0bb-117">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fd0bb-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fd0bb-118">Requirements</span></span>



| <span data-ttu-id="fd0bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fd0bb-119">Requirement</span></span> | <span data-ttu-id="fd0bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fd0bb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0bb-121">Header</span><span class="sxs-lookup"><span data-stu-id="fd0bb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fd0bb-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0bb-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd0bb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd0bb-123">Library</span></span><br/> | <dl> <span data-ttu-id="fd0bb-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd0bb-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd0bb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd0bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0bb-126">Математические функции</span><span class="sxs-lookup"><span data-stu-id="fd0bb-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
