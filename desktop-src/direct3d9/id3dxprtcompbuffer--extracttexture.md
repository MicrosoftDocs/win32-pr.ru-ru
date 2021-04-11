---
description: Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных ID3DXPRTCompBuffer и добавляет их в объект IDirect3DTexture9.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'Метод ID3DXPRTCompBuffer:: Екстракттекстуре (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081890"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="f320a-103">Метод ID3DXPRTCompBuffer:: Екстракттекстуре</span><span class="sxs-lookup"><span data-stu-id="f320a-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="f320a-104">Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) и добавляет их в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="f320a-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f320a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f320a-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f320a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f320a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f320a-107">*Стартпка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f320a-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f320a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f320a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f320a-109">Начальное значение коэффициента буфера, из которого извлекаются данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="f320a-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="f320a-110">*Нумпка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f320a-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f320a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f320a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f320a-112">Количество коэффициентов PCA для извлечения из буфера.</span><span class="sxs-lookup"><span data-stu-id="f320a-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f320a-113">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f320a-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f320a-114">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f320a-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f320a-115">Указатель на объект текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , в котором будут храниться коэффициенты PCA.</span><span class="sxs-lookup"><span data-stu-id="f320a-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f320a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f320a-116">Return value</span></span>

<span data-ttu-id="f320a-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f320a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f320a-118">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f320a-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f320a-119">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="f320a-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f320a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f320a-120">Requirements</span></span>



| <span data-ttu-id="f320a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f320a-121">Requirement</span></span> | <span data-ttu-id="f320a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f320a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f320a-123">Header</span><span class="sxs-lookup"><span data-stu-id="f320a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f320a-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f320a-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f320a-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f320a-125">Library</span></span><br/> | <dl> <span data-ttu-id="f320a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f320a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f320a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f320a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f320a-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="f320a-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
