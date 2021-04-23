---
description: Отмена сопоставления буфера.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'Метод ID3DX10MeshBuffer:: unотмена (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c3b382e0cfd01a51d89ddacb51ad390446315a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694360"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="9d8f0-103">Метод ID3DX10MeshBuffer:: unотмена</span><span class="sxs-lookup"><span data-stu-id="9d8f0-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="9d8f0-104">Отмена сопоставления буфера.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d8f0-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="9d8f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d8f0-106">Parameters</span></span>

<span data-ttu-id="9d8f0-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d8f0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d8f0-108">Return value</span></span>

<span data-ttu-id="9d8f0-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d8f0-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d8f0-110">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f0-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d8f0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d8f0-111">Remarks</span></span>



|                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8f0-112">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9d8f0-112">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="9d8f0-113">Отмена сопоставления () в Direct3D 10 аналогична разблокировке ресурсов () в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="9d8f0-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d8f0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9d8f0-114">Requirements</span></span>



| <span data-ttu-id="9d8f0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9d8f0-115">Requirement</span></span> | <span data-ttu-id="9d8f0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9d8f0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8f0-117">Header</span><span class="sxs-lookup"><span data-stu-id="9d8f0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9d8f0-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d8f0-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d8f0-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d8f0-119">Library</span></span><br/> | <dl> <span data-ttu-id="9d8f0-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d8f0-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d8f0-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d8f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d8f0-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="9d8f0-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="9d8f0-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="9d8f0-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




