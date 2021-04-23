---
description: Возвращает максимальное количество влияния на любую вершину в сетке.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'Метод ID3DXSkinInfo:: Жетмаксвертексинфлуенцес (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acae5cc119df25989e6bf22692ec1609ffa9408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000304"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a><span data-ttu-id="a073c-103">Метод ID3DXSkinInfo:: Жетмаксвертексинфлуенцес</span><span class="sxs-lookup"><span data-stu-id="a073c-103">ID3DXSkinInfo::GetMaxVertexInfluences method</span></span>

<span data-ttu-id="a073c-104">Возвращает максимальное количество влияния на любую вершину в сетке.</span><span class="sxs-lookup"><span data-stu-id="a073c-104">Gets the maximum number of influences for any vertex in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a073c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a073c-105">Syntax</span></span>


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="a073c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a073c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a073c-107">*максвертексинфлуенцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a073c-107">*maxVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a073c-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a073c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a073c-109">Указатель на максимальную влияние на вершину.</span><span class="sxs-lookup"><span data-stu-id="a073c-109">Pointer to the maximum vertex influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a073c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a073c-110">Return value</span></span>

<span data-ttu-id="a073c-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a073c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a073c-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a073c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a073c-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a073c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a073c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a073c-114">Requirements</span></span>



| <span data-ttu-id="a073c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a073c-115">Requirement</span></span> | <span data-ttu-id="a073c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a073c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a073c-117">Header</span><span class="sxs-lookup"><span data-stu-id="a073c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a073c-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a073c-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a073c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a073c-119">Library</span></span><br/> | <dl> <span data-ttu-id="a073c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a073c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a073c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a073c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a073c-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="a073c-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
