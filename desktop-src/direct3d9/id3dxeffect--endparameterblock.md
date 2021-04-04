---
description: Прерывать изменения состояния параметров эффектов записи.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'Метод ID3DXEffect:: Ендпараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000382"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="89d81-103">Метод ID3DXEffect:: Ендпараметерблокк</span><span class="sxs-lookup"><span data-stu-id="89d81-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="89d81-104">Прерывать изменения состояния параметров эффектов записи.</span><span class="sxs-lookup"><span data-stu-id="89d81-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d81-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="89d81-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89d81-106">Parameters</span></span>

<span data-ttu-id="89d81-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="89d81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89d81-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89d81-108">Return value</span></span>

<span data-ttu-id="89d81-109">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="89d81-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="89d81-110">Возвращает маркер в блок состояния параметра.</span><span class="sxs-lookup"><span data-stu-id="89d81-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d81-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89d81-111">Remarks</span></span>

<span data-ttu-id="89d81-112">Все параметры эффектов, изменяющие состояние (после вызова Бегинпараметерблокк и до вызова Ендпараметерблокк), будут сохранены в блоке состояния параметра effect.</span><span class="sxs-lookup"><span data-stu-id="89d81-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="89d81-113">Используйте Апплипараметерблокк, чтобы применить этот блок изменений состояния к системе эффектов.</span><span class="sxs-lookup"><span data-stu-id="89d81-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="89d81-114">После завершения работы с блоком состояния используйте Делетепараметерблокк, чтобы освободить память.</span><span class="sxs-lookup"><span data-stu-id="89d81-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d81-115">Требования</span><span class="sxs-lookup"><span data-stu-id="89d81-115">Requirements</span></span>



| <span data-ttu-id="89d81-116">Требование</span><span class="sxs-lookup"><span data-stu-id="89d81-116">Requirement</span></span> | <span data-ttu-id="89d81-117">Значение</span><span class="sxs-lookup"><span data-stu-id="89d81-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d81-118">Header</span><span class="sxs-lookup"><span data-stu-id="89d81-118">Header</span></span><br/>  | <dl> <span data-ttu-id="89d81-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d81-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="89d81-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89d81-120">Library</span></span><br/> | <dl> <span data-ttu-id="89d81-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89d81-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="89d81-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89d81-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d81-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="89d81-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="89d81-124">**ID3DXEffect:: Бегинпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="89d81-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="89d81-125">**ID3DXEffect:: Апплипараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="89d81-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="89d81-126">**ID3DXEffect::D Елетепараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="89d81-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




