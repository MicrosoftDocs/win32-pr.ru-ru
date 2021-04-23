---
description: Извлекает описание поверхности рендеринга.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'Метод ID3DXRenderToEnvMap:: desc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821020"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="63d73-103">Метод ID3DXRenderToEnvMap:: DESC</span><span class="sxs-lookup"><span data-stu-id="63d73-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="63d73-104">Извлекает описание поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="63d73-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63d73-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="63d73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d73-107">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63d73-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63d73-108">Тип: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="63d73-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="63d73-109">Указатель на структуру [**D3DXRTE \_ DESC**](d3dxrte-desc.md) , описывающую поверхность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="63d73-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d73-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63d73-110">Return value</span></span>

<span data-ttu-id="63d73-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63d73-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63d73-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="63d73-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="63d73-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="63d73-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d73-114">Требования</span><span class="sxs-lookup"><span data-stu-id="63d73-114">Requirements</span></span>



| <span data-ttu-id="63d73-115">Требование</span><span class="sxs-lookup"><span data-stu-id="63d73-115">Requirement</span></span> | <span data-ttu-id="63d73-116">Значение</span><span class="sxs-lookup"><span data-stu-id="63d73-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63d73-117">Header</span><span class="sxs-lookup"><span data-stu-id="63d73-117">Header</span></span><br/>  | <dl> <span data-ttu-id="63d73-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="63d73-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="63d73-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63d73-119">Library</span></span><br/> | <dl> <span data-ttu-id="63d73-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63d73-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63d73-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63d73-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d73-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="63d73-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




