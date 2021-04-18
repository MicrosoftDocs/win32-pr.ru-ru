---
description: Установите данные точки для сетки.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'Метод ID3DX10Mesh:: Сетпоинтрепдата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713841"
---
# <a name="id3dx10meshsetpointrepdata-method"></a><span data-ttu-id="ffbd5-103">Метод ID3DX10Mesh:: Сетпоинтрепдата</span><span class="sxs-lookup"><span data-stu-id="ffbd5-103">ID3DX10Mesh::SetPointRepData method</span></span>

<span data-ttu-id="ffbd5-104">Установите данные точки для сетки.</span><span class="sxs-lookup"><span data-stu-id="ffbd5-104">Set the point rep data for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbd5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffbd5-105">Syntax</span></span>


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="ffbd5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffbd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffbd5-107">*ппоинтрепс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffbd5-107">*pPointReps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffbd5-108">Тип: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ffbd5-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ffbd5-109">Устанавливаемые данные Point.</span><span class="sxs-lookup"><span data-stu-id="ffbd5-109">The point rep data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffbd5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffbd5-110">Return value</span></span>

<span data-ttu-id="ffbd5-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ffbd5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ffbd5-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ffbd5-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbd5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ffbd5-113">Requirements</span></span>



| <span data-ttu-id="ffbd5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ffbd5-114">Requirement</span></span> | <span data-ttu-id="ffbd5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ffbd5-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbd5-116">Header</span><span class="sxs-lookup"><span data-stu-id="ffbd5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ffbd5-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffbd5-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffbd5-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ffbd5-118">Library</span></span><br/> | <dl> <span data-ttu-id="ffbd5-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffbd5-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffbd5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffbd5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbd5-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ffbd5-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ffbd5-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ffbd5-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
