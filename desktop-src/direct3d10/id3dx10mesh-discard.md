---
description: 'Удаляет данные сетки с устройства, которое было зафиксировано на устройстве (с помощью ID3DX10Mesh:: Коммиттодевице).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: 'ID3DX10Mesh: метод:D-карты (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674700"
---
# <a name="id3dx10meshdiscard-method"></a><span data-ttu-id="50a6d-103">ID3DX10Mesh::D методе кредитной карты</span><span class="sxs-lookup"><span data-stu-id="50a6d-103">ID3DX10Mesh::Discard method</span></span>

<span data-ttu-id="50a6d-104">Удаляет данные сетки с устройства, которое было зафиксировано на устройстве (с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="50a6d-104">Removes mesh data from the device that has been committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="50a6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50a6d-105">Syntax</span></span>


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a><span data-ttu-id="50a6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50a6d-107">*двдискард* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50a6d-107">*dwDiscard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a6d-108">Тип: **[ **\_ \_ \_ Флаги удаления сетки D3DX10**](d3dx10-mesh-discard-flags.md)**</span><span class="sxs-lookup"><span data-stu-id="50a6d-108">Type: **[**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md)**</span></span>

<span data-ttu-id="50a6d-109">Указывает, какие части данных сетки следует отбросить от устройства.</span><span class="sxs-lookup"><span data-stu-id="50a6d-109">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="50a6d-110">См. раздел [**\_ \_ \_ Флаги отказа в сетке D3DX10**](d3dx10-mesh-discard-flags.md).</span><span class="sxs-lookup"><span data-stu-id="50a6d-110">See [**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50a6d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50a6d-111">Return value</span></span>

<span data-ttu-id="50a6d-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50a6d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50a6d-113">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="50a6d-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50a6d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="50a6d-114">Requirements</span></span>



| <span data-ttu-id="50a6d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="50a6d-115">Requirement</span></span> | <span data-ttu-id="50a6d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="50a6d-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50a6d-117">Header</span><span class="sxs-lookup"><span data-stu-id="50a6d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="50a6d-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a6d-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="50a6d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50a6d-119">Library</span></span><br/> | <dl> <span data-ttu-id="50a6d-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50a6d-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50a6d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50a6d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a6d-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="50a6d-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="50a6d-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="50a6d-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




