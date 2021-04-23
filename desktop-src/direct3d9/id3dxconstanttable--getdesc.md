---
description: Возвращает описание таблицы констант.
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'Метод ID3DXConstantTable:: desc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71eeb951ec73fbeb9942f52e30ab9ad59e374ee7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914736"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="ead4f-103">Метод ID3DXConstantTable:: DESC</span><span class="sxs-lookup"><span data-stu-id="ead4f-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="ead4f-104">Возвращает описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="ead4f-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ead4f-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ead4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ead4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead4f-107">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ead4f-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead4f-108">Тип: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ead4f-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="ead4f-109">Описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="ead4f-109">Description of the constant table.</span></span> <span data-ttu-id="ead4f-110">См. [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="ead4f-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead4f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ead4f-111">Return value</span></span>

<span data-ttu-id="ead4f-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ead4f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ead4f-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ead4f-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ead4f-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ead4f-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead4f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ead4f-115">Requirements</span></span>



| <span data-ttu-id="ead4f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ead4f-116">Requirement</span></span> | <span data-ttu-id="ead4f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ead4f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead4f-118">Header</span><span class="sxs-lookup"><span data-stu-id="ead4f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ead4f-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead4f-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ead4f-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ead4f-120">Library</span></span><br/> | <dl> <span data-ttu-id="ead4f-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ead4f-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ead4f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ead4f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead4f-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ead4f-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="ead4f-124">**ID3DXConstantTable:: Жетконстантдеск**</span><span class="sxs-lookup"><span data-stu-id="ead4f-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




