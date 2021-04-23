---
description: Извлекает данные коэффициента из цветового канала буфера для указанного диапазона коэффициентов и добавляет данные в объект IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'Метод ID3DXPRTBuffer:: Екстракттекстуре (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000412"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="8a6cd-103">Метод ID3DXPRTBuffer:: Екстракттекстуре</span><span class="sxs-lookup"><span data-stu-id="8a6cd-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="8a6cd-104">Извлекает данные коэффициента из цветового канала буфера для указанного диапазона коэффициентов и добавляет данные в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="8a6cd-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a6cd-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="8a6cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6cd-107">*Канал* \[ связи окне\]</span><span class="sxs-lookup"><span data-stu-id="8a6cd-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6cd-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a6cd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a6cd-109">Канал цвета буфера, из которого извлекаются данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="8a6cd-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8a6cd-110">*СтарткоеффиЦиент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a6cd-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6cd-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a6cd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a6cd-112">Начальное значение коэффициента буфера, из которого извлекаются данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="8a6cd-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8a6cd-113">*НумкоеффиЦиентс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a6cd-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6cd-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a6cd-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a6cd-115">Число скаляров, начиная с СтарткоеффиЦиент, из которого извлекаются данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="8a6cd-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8a6cd-116">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a6cd-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6cd-117">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="8a6cd-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="8a6cd-118">Указатель на объект текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , который будет хранить коэффициенты.</span><span class="sxs-lookup"><span data-stu-id="8a6cd-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a6cd-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a6cd-119">Return value</span></span>

<span data-ttu-id="8a6cd-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a6cd-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a6cd-121">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="8a6cd-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8a6cd-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8a6cd-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6cd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8a6cd-123">Requirements</span></span>



| <span data-ttu-id="8a6cd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8a6cd-124">Requirement</span></span> | <span data-ttu-id="8a6cd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8a6cd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6cd-126">Header</span><span class="sxs-lookup"><span data-stu-id="8a6cd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8a6cd-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a6cd-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8a6cd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a6cd-128">Library</span></span><br/> | <dl> <span data-ttu-id="8a6cd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a6cd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a6cd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a6cd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6cd-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="8a6cd-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
