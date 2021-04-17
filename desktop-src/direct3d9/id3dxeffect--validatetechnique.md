---
description: Проверка метода.
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'Метод ID3DXEffect:: Валидатетечникуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703697"
---
# <a name="id3dxeffectvalidatetechnique-method"></a><span data-ttu-id="6c389-103">Метод ID3DXEffect:: Валидатетечникуе</span><span class="sxs-lookup"><span data-stu-id="6c389-103">ID3DXEffect::ValidateTechnique method</span></span>

<span data-ttu-id="6c389-104">Проверка метода.</span><span class="sxs-lookup"><span data-stu-id="6c389-104">Validate a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c389-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c389-105">Syntax</span></span>


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="6c389-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c389-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c389-107">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c389-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c389-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6c389-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6c389-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="6c389-109">Unique identifier.</span></span> <span data-ttu-id="6c389-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6c389-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c389-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c389-111">Return value</span></span>

<span data-ttu-id="6c389-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c389-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c389-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6c389-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c389-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ КОНФЛИКТИНГРЕНДЕРСТАТЕ, D3DERR \_ конфликтингтекстурефилтер, D3DERR \_ девицелост, D3DERR \_ ДРИВЕРИНТЕРНАЛЕРРОР, D3DERR \_ TOOMANYOPERATIONS, D3DERR \_ UNSUPPORTEDALPHAARG, D3DERR \_ UNSUPPORTEDALPHAOPERATION, D3DERR \_ UNSUPPORTEDCOLORARG, D3DERR \_ UNSUPPORTEDCOLOROPERATION, D3DERR \_ UNSUPPORTEDFACTORVALUE, D3DERR \_ UNSUPPORTEDTEXTUREFILTER и D3DERR \_ WRONGTEXTUREFORMAT.</span><span class="sxs-lookup"><span data-stu-id="6c389-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_CONFLICTINGRENDERSTATE, D3DERR\_CONFLICTINGTEXTUREFILTER, D3DERR\_DEVICELOST, D3DERR\_DRIVERINTERNALERROR, D3DERR\_TOOMANYOPERATIONS, D3DERR\_UNSUPPORTEDALPHAARG, D3DERR\_UNSUPPORTEDALPHAOPERATION, D3DERR\_UNSUPPORTEDCOLORARG, D3DERR\_UNSUPPORTEDCOLOROPERATION, D3DERR\_UNSUPPORTEDFACTORVALUE, D3DERR\_UNSUPPORTEDTEXTUREFILTER, and D3DERR\_WRONGTEXTUREFORMAT.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c389-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6c389-115">Requirements</span></span>



| <span data-ttu-id="6c389-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6c389-116">Requirement</span></span> | <span data-ttu-id="6c389-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6c389-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c389-118">Header</span><span class="sxs-lookup"><span data-stu-id="6c389-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6c389-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c389-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6c389-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c389-120">Library</span></span><br/> | <dl> <span data-ttu-id="6c389-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c389-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6c389-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c389-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c389-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="6c389-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="6c389-124">**ID3DXEffect:: Сеттечникуе**</span><span class="sxs-lookup"><span data-stu-id="6c389-124">**ID3DXEffect::SetTechnique**</span></span>](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




