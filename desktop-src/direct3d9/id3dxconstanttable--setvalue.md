---
description: Устанавливает содержимое буфера в таблицу констант.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'Метод ID3DXConstantTable:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703809"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="80978-103">Метод ID3DXConstantTable:: SetValue</span><span class="sxs-lookup"><span data-stu-id="80978-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="80978-104">Устанавливает содержимое буфера в таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="80978-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="80978-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80978-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="80978-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80978-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80978-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80978-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="80978-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="80978-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="80978-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="80978-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80978-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80978-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="80978-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="80978-112">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="80978-112">Unique identifier to a constant.</span></span> <span data-ttu-id="80978-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="80978-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="80978-114">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80978-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80978-115">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80978-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80978-116">Буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="80978-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="80978-117">*Байт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80978-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80978-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80978-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80978-119">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="80978-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80978-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80978-120">Return value</span></span>

<span data-ttu-id="80978-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80978-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80978-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="80978-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80978-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="80978-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="80978-124">Требования</span><span class="sxs-lookup"><span data-stu-id="80978-124">Requirements</span></span>



| <span data-ttu-id="80978-125">Требование</span><span class="sxs-lookup"><span data-stu-id="80978-125">Requirement</span></span> | <span data-ttu-id="80978-126">Значение</span><span class="sxs-lookup"><span data-stu-id="80978-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80978-127">Header</span><span class="sxs-lookup"><span data-stu-id="80978-127">Header</span></span><br/>  | <dl> <span data-ttu-id="80978-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="80978-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="80978-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80978-129">Library</span></span><br/> | <dl> <span data-ttu-id="80978-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80978-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="80978-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80978-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80978-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="80978-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
