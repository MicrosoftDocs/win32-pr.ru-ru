---
description: 'Метод ID3DXTextureShader:: Жетконстантбинаме — возвращает константу путем поиска ее имени.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'Метод ID3DXTextureShader:: Жетконстантбинаме (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117662"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="f404a-103">Метод ID3DXTextureShader:: Жетконстантбинаме</span><span class="sxs-lookup"><span data-stu-id="f404a-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="f404a-104">Возвращает константу путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="f404a-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f404a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f404a-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="f404a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f404a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f404a-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f404a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f404a-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f404a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f404a-109">[Маркер](handles.md) родительской структуры данных.</span><span class="sxs-lookup"><span data-stu-id="f404a-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="f404a-110">Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f404a-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f404a-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f404a-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f404a-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f404a-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f404a-113">Строка, содержащая имя константы.</span><span class="sxs-lookup"><span data-stu-id="f404a-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f404a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f404a-114">Return value</span></span>

<span data-ttu-id="f404a-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f404a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f404a-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="f404a-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="f404a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f404a-117">Requirements</span></span>



| <span data-ttu-id="f404a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f404a-118">Requirement</span></span> | <span data-ttu-id="f404a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f404a-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f404a-120">Header</span><span class="sxs-lookup"><span data-stu-id="f404a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f404a-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f404a-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f404a-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f404a-122">Library</span></span><br/> | <dl> <span data-ttu-id="f404a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f404a-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f404a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f404a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f404a-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="f404a-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
