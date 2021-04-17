---
description: Возвращает маркер функции.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: Метод ID3DXBaseEffect::-Function (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: de0567b605f4a892c1f8274a346a74acfbbc0442
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703996"
---
# <a name="id3dxbaseeffectgetfunction-method"></a><span data-ttu-id="7bcc4-103">Метод ID3DXBaseEffect:: Function</span><span class="sxs-lookup"><span data-stu-id="7bcc4-103">ID3DXBaseEffect::GetFunction method</span></span>

<span data-ttu-id="7bcc4-104">Возвращает маркер функции.</span><span class="sxs-lookup"><span data-stu-id="7bcc4-104">Gets the handle of a function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bcc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bcc4-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="7bcc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bcc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bcc4-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7bcc4-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bcc4-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7bcc4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7bcc4-109">Индекс функции.</span><span class="sxs-lookup"><span data-stu-id="7bcc4-109">Function index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bcc4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bcc4-110">Return value</span></span>

<span data-ttu-id="7bcc4-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7bcc4-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7bcc4-112">Возвращает маркер указанной функции или **значение NULL** , если индекс является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="7bcc4-112">Returns the handle of the specified function, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="7bcc4-113">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7bcc4-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bcc4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7bcc4-114">Requirements</span></span>



| <span data-ttu-id="7bcc4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7bcc4-115">Requirement</span></span> | <span data-ttu-id="7bcc4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7bcc4-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bcc4-117">Header</span><span class="sxs-lookup"><span data-stu-id="7bcc4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7bcc4-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bcc4-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7bcc4-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7bcc4-119">Library</span></span><br/> | <dl> <span data-ttu-id="7bcc4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bcc4-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7bcc4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bcc4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bcc4-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7bcc4-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
