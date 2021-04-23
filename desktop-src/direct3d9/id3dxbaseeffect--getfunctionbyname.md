---
description: Возвращает маркер функции путем поиска ее имени.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'Метод ID3DXBaseEffect:: Жетфунктионбинаме (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355910"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="c00c9-103">Метод ID3DXBaseEffect:: Жетфунктионбинаме</span><span class="sxs-lookup"><span data-stu-id="c00c9-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="c00c9-104">Возвращает маркер функции путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="c00c9-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c00c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c00c9-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="c00c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c00c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c00c9-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c00c9-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c00c9-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c00c9-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c00c9-109">Строка, содержащая имя функции.</span><span class="sxs-lookup"><span data-stu-id="c00c9-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c00c9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c00c9-110">Return value</span></span>

<span data-ttu-id="c00c9-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c00c9-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c00c9-112">Возвращает маркер указанной функции или **значение NULL** , если имя не найдено.</span><span class="sxs-lookup"><span data-stu-id="c00c9-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="c00c9-113">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c00c9-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c00c9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c00c9-114">Requirements</span></span>



| <span data-ttu-id="c00c9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c00c9-115">Requirement</span></span> | <span data-ttu-id="c00c9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c00c9-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c00c9-117">Header</span><span class="sxs-lookup"><span data-stu-id="c00c9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c00c9-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c00c9-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c00c9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c00c9-119">Library</span></span><br/> | <dl> <span data-ttu-id="c00c9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c00c9-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c00c9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c00c9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00c9-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c00c9-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
