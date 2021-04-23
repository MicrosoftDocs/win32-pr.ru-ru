---
description: Задает число с плавающей запятой.
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'Метод ID3DXConstantTable:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694185"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="a7d1a-103">Метод ID3DXConstantTable:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="a7d1a-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="a7d1a-104">Задает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a7d1a-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7d1a-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="a7d1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7d1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d1a-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7d1a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d1a-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a7d1a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a7d1a-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="a7d1a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a7d1a-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7d1a-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d1a-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d1a-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a7d1a-112">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="a7d1a-112">Unique identifier to the constant.</span></span> <span data-ttu-id="a7d1a-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a7d1a-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d1a-114">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a7d1a-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d1a-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d1a-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7d1a-116">Число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a7d1a-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d1a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7d1a-117">Return value</span></span>

<span data-ttu-id="a7d1a-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7d1a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7d1a-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a7d1a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7d1a-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a7d1a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d1a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a7d1a-121">Requirements</span></span>



| <span data-ttu-id="a7d1a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a7d1a-122">Requirement</span></span> | <span data-ttu-id="a7d1a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a7d1a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d1a-124">Header</span><span class="sxs-lookup"><span data-stu-id="a7d1a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d1a-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7d1a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a7d1a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7d1a-126">Library</span></span><br/> | <dl> <span data-ttu-id="a7d1a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7d1a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a7d1a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7d1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d1a-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a7d1a-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
