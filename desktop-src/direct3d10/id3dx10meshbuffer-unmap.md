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
ms.openlocfilehash: 11b15f8bc1e4103503b183672ebd31e92b4daea7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335378"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="87911-103">Метод ID3DX10MeshBuffer:: unотмена</span><span class="sxs-lookup"><span data-stu-id="87911-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="87911-104">Отмена сопоставления буфера.</span><span class="sxs-lookup"><span data-stu-id="87911-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="87911-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87911-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="87911-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87911-106">Parameters</span></span>

<span data-ttu-id="87911-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="87911-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87911-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87911-108">Return value</span></span>

<span data-ttu-id="87911-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87911-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87911-110">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="87911-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87911-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87911-111">Remarks</span></span>



<span data-ttu-id="87911-112">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="87911-112">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="87911-113">Отмена сопоставления () в Direct3D 10 аналогична разблокировке ресурсов () в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="87911-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="87911-114">Требования</span><span class="sxs-lookup"><span data-stu-id="87911-114">Requirements</span></span>



| <span data-ttu-id="87911-115">Требование</span><span class="sxs-lookup"><span data-stu-id="87911-115">Requirement</span></span> | <span data-ttu-id="87911-116">Значение</span><span class="sxs-lookup"><span data-stu-id="87911-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87911-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="87911-117">Header</span></span><br/>  | <dl> <span data-ttu-id="87911-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="87911-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="87911-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87911-119">Library</span></span><br/> | <dl> <span data-ttu-id="87911-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87911-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87911-121">См. также</span><span class="sxs-lookup"><span data-stu-id="87911-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87911-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="87911-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="87911-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="87911-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




