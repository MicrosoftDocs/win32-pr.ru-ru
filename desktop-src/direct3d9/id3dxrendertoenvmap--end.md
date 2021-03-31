---
description: Восстановите все целевые объекты отрисовки и при необходимости сформируйте все отрисованные лица в области схемы среды.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'Метод ID3DXRenderToEnvMap:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354563"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="db8ae-103">Метод ID3DXRenderToEnvMap:: end</span><span class="sxs-lookup"><span data-stu-id="db8ae-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="db8ae-104">Восстановите все целевые объекты отрисовки и при необходимости сформируйте все отрисованные лица в области схемы среды.</span><span class="sxs-lookup"><span data-stu-id="db8ae-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db8ae-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="db8ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db8ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db8ae-107">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db8ae-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8ae-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db8ae-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db8ae-109">Допустимое сочетание одного или нескольких флагов [ \_ фильтра D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="db8ae-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db8ae-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db8ae-110">Return value</span></span>

<span data-ttu-id="db8ae-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db8ae-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db8ae-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="db8ae-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db8ae-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="db8ae-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="db8ae-114">Требования</span><span class="sxs-lookup"><span data-stu-id="db8ae-114">Requirements</span></span>



| <span data-ttu-id="db8ae-115">Требование</span><span class="sxs-lookup"><span data-stu-id="db8ae-115">Requirement</span></span> | <span data-ttu-id="db8ae-116">Значение</span><span class="sxs-lookup"><span data-stu-id="db8ae-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db8ae-117">Header</span><span class="sxs-lookup"><span data-stu-id="db8ae-117">Header</span></span><br/>  | <dl> <span data-ttu-id="db8ae-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="db8ae-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="db8ae-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db8ae-119">Library</span></span><br/> | <dl> <span data-ttu-id="db8ae-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db8ae-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db8ae-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db8ae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8ae-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="db8ae-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="db8ae-123">**ID3DXRenderToEnvMap:: Face**</span><span class="sxs-lookup"><span data-stu-id="db8ae-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
