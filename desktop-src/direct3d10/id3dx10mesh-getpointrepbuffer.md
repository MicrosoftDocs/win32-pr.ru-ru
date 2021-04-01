---
description: Получает буфер торгового представителя сетки.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'Метод ID3DX10Mesh:: Жетпоинтрепбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157195"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="ccbef-103">Метод ID3DX10Mesh:: Жетпоинтрепбуффер</span><span class="sxs-lookup"><span data-stu-id="ccbef-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="ccbef-104">Получает буфер торгового представителя сетки.</span><span class="sxs-lookup"><span data-stu-id="ccbef-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccbef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccbef-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="ccbef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccbef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccbef-107">*пппоинтрепс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ccbef-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbef-108">Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ccbef-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="ccbef-109">Указатель на буфер сетки, содержащий данные о геообъектной сетке сетки.</span><span class="sxs-lookup"><span data-stu-id="ccbef-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="ccbef-110">См. [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ccbef-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccbef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccbef-111">Return value</span></span>

<span data-ttu-id="ccbef-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccbef-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccbef-113">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ccbef-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbef-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ccbef-114">Requirements</span></span>



| <span data-ttu-id="ccbef-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ccbef-115">Requirement</span></span> | <span data-ttu-id="ccbef-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ccbef-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbef-117">Header</span><span class="sxs-lookup"><span data-stu-id="ccbef-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ccbef-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccbef-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccbef-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ccbef-119">Library</span></span><br/> | <dl> <span data-ttu-id="ccbef-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccbef-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccbef-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccbef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccbef-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ccbef-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ccbef-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ccbef-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




