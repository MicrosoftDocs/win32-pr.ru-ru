---
description: Задает активный метод.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'Метод ID3DXEffect:: Сеттечникуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000322"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="de4ea-103">Метод ID3DXEffect:: Сеттечникуе</span><span class="sxs-lookup"><span data-stu-id="de4ea-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="de4ea-104">Задает активный метод.</span><span class="sxs-lookup"><span data-stu-id="de4ea-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de4ea-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="de4ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de4ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4ea-107">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de4ea-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de4ea-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="de4ea-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="de4ea-109">Уникальный описатель для метода.</span><span class="sxs-lookup"><span data-stu-id="de4ea-109">Unique handle to the technique.</span></span> <span data-ttu-id="de4ea-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="de4ea-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4ea-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de4ea-111">Return value</span></span>

<span data-ttu-id="de4ea-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de4ea-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de4ea-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="de4ea-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="de4ea-114">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="de4ea-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4ea-115">Требования</span><span class="sxs-lookup"><span data-stu-id="de4ea-115">Requirements</span></span>



| <span data-ttu-id="de4ea-116">Требование</span><span class="sxs-lookup"><span data-stu-id="de4ea-116">Requirement</span></span> | <span data-ttu-id="de4ea-117">Значение</span><span class="sxs-lookup"><span data-stu-id="de4ea-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4ea-118">Header</span><span class="sxs-lookup"><span data-stu-id="de4ea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="de4ea-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="de4ea-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="de4ea-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de4ea-120">Library</span></span><br/> | <dl> <span data-ttu-id="de4ea-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de4ea-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="de4ea-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de4ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4ea-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="de4ea-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




