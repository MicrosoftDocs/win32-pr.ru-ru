---
description: Создает копию результата.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'Метод ID3DXEffect:: Клониффект (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713720"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="8e780-103">Метод ID3DXEffect:: Клониффект</span><span class="sxs-lookup"><span data-stu-id="8e780-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="8e780-104">Создает копию результата.</span><span class="sxs-lookup"><span data-stu-id="8e780-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e780-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e780-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="8e780-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e780-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e780-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e780-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8e780-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8e780-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с этим действием.</span><span class="sxs-lookup"><span data-stu-id="8e780-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="8e780-110">*ппеффект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8e780-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e780-111">Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e780-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="8e780-112">Указатель на интерфейс [**ID3DXEffect**](id3dxeffect.md) , содержащий клонированный результат.</span><span class="sxs-lookup"><span data-stu-id="8e780-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e780-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e780-113">Return value</span></span>

<span data-ttu-id="8e780-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e780-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e780-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="8e780-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8e780-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8e780-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e780-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e780-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8e780-118">Эта функция не будет клонировать результат, если пользователь указывает, что [D3DXFX \_ не может \_ клонироваться](d3dxfx.md) во время создания результата.</span><span class="sxs-lookup"><span data-stu-id="8e780-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="8e780-119">Сведения об обновлении общих и необщих параметров в активном методе клонированного результата см. в разделе [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md).</span><span class="sxs-lookup"><span data-stu-id="8e780-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e780-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8e780-120">Requirements</span></span>



| <span data-ttu-id="8e780-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8e780-121">Requirement</span></span> | <span data-ttu-id="8e780-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8e780-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e780-123">Header</span><span class="sxs-lookup"><span data-stu-id="8e780-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8e780-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e780-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8e780-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e780-125">Library</span></span><br/> | <dl> <span data-ttu-id="8e780-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e780-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8e780-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e780-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e780-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8e780-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
