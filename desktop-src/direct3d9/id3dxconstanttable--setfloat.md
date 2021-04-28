---
description: 'Метод ID3DXConstantTable:: SetFloat — задает число с плавающей запятой.'
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
ms.openlocfilehash: 6589d56e0b9dcf8debe14a7c81f86a4972a73405
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115222"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="8e9af-103">Метод ID3DXConstantTable:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="8e9af-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="8e9af-104">Задает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="8e9af-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e9af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e9af-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="8e9af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e9af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e9af-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e9af-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e9af-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8e9af-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8e9af-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="8e9af-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="8e9af-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e9af-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e9af-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8e9af-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8e9af-112">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="8e9af-112">Unique identifier to the constant.</span></span> <span data-ttu-id="8e9af-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8e9af-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e9af-114">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8e9af-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e9af-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e9af-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e9af-116">Число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="8e9af-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e9af-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e9af-117">Return value</span></span>

<span data-ttu-id="8e9af-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e9af-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e9af-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8e9af-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8e9af-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="8e9af-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e9af-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8e9af-121">Requirements</span></span>



| <span data-ttu-id="8e9af-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8e9af-122">Requirement</span></span> | <span data-ttu-id="8e9af-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9af-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9af-124">Header</span><span class="sxs-lookup"><span data-stu-id="8e9af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8e9af-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e9af-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8e9af-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e9af-126">Library</span></span><br/> | <dl> <span data-ttu-id="8e9af-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e9af-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8e9af-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8e9af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e9af-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="8e9af-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
