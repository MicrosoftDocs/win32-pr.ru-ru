---
description: Возвращает описание таблицы констант.
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'Метод ID3DXTextureShader:: desc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97302b7e0f8c9f05e6229e20c2c9c158173ed944
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273804"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="ee872-103">Метод ID3DXTextureShader:: DESC</span><span class="sxs-lookup"><span data-stu-id="ee872-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="ee872-104">Возвращает описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="ee872-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee872-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee872-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ee872-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee872-107">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee872-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee872-108">Тип: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee872-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="ee872-109">Атрибуты таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="ee872-109">The attributes of the constant table.</span></span> <span data-ttu-id="ee872-110">См. [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="ee872-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee872-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee872-111">Return value</span></span>

<span data-ttu-id="ee872-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee872-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee872-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ee872-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee872-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ee872-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee872-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ee872-115">Requirements</span></span>



| <span data-ttu-id="ee872-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ee872-116">Requirement</span></span> | <span data-ttu-id="ee872-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ee872-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee872-118">Header</span><span class="sxs-lookup"><span data-stu-id="ee872-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ee872-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee872-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ee872-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee872-120">Library</span></span><br/> | <dl> <span data-ttu-id="ee872-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee872-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ee872-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee872-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee872-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ee872-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




