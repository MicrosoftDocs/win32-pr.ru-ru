---
description: Возвращает константу путем поиска ее имени.
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
ms.openlocfilehash: a285da2fa3179f91d34eda8d9ce1f622c86df15b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703937"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="8d7c8-103">Метод ID3DXTextureShader:: Жетконстантбинаме</span><span class="sxs-lookup"><span data-stu-id="8d7c8-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="8d7c8-104">Возвращает константу путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="8d7c8-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d7c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d7c8-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="8d7c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d7c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d7c8-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d7c8-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d7c8-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8d7c8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8d7c8-109">[Маркер](handles.md) родительской структуры данных.</span><span class="sxs-lookup"><span data-stu-id="8d7c8-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="8d7c8-110">Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8d7c8-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d7c8-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d7c8-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d7c8-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d7c8-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d7c8-113">Строка, содержащая имя константы.</span><span class="sxs-lookup"><span data-stu-id="8d7c8-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d7c8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d7c8-114">Return value</span></span>

<span data-ttu-id="8d7c8-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8d7c8-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8d7c8-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="8d7c8-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d7c8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8d7c8-117">Requirements</span></span>



| <span data-ttu-id="8d7c8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8d7c8-118">Requirement</span></span> | <span data-ttu-id="8d7c8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7c8-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7c8-120">Header</span><span class="sxs-lookup"><span data-stu-id="8d7c8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8d7c8-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c8-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8d7c8-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d7c8-122">Library</span></span><br/> | <dl> <span data-ttu-id="8d7c8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c8-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8d7c8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d7c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7c8-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8d7c8-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
