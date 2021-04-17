---
description: Реализованный пользователем метод для закрытия файла включения шейдера \# .
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'Метод ID3DXInclude:: Close (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694301"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="9a8f5-103">Метод ID3DXInclude:: Close</span><span class="sxs-lookup"><span data-stu-id="9a8f5-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="9a8f5-104">Реализованный пользователем метод для закрытия файла включения шейдера \# .</span><span class="sxs-lookup"><span data-stu-id="9a8f5-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a8f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a8f5-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="9a8f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a8f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a8f5-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a8f5-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a8f5-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a8f5-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a8f5-109">Указатель на возвращаемый буфер, содержащий директивы include.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="9a8f5-110">Это указатель, возвращенный соответствующим вызовом [**ID3DXInclude:: Open**](id3dxinclude--open.md) .</span><span class="sxs-lookup"><span data-stu-id="9a8f5-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a8f5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a8f5-111">Return value</span></span>

<span data-ttu-id="9a8f5-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a8f5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a8f5-113">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="9a8f5-114">Если при чтении включаемого файла происходит сбой обратного вызова \# , то API-интерфейс, который вызвал вызов функции обратного вызова, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="9a8f5-115">Возможны следующие варианты.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-115">This is one of the following:</span></span>

-   <span data-ttu-id="9a8f5-116">Шейдер HLSL не сможет выполнить одну из \* \* \* функций D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="9a8f5-117">Шейдер сборки завершится ошибкой одной из \* \* \* функций D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="9a8f5-118">Этот результат приведет к сбою одной из \* \* \* функций D3DXCreateEffect или D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="9a8f5-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a8f5-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a8f5-119">Remarks</span></span>

<span data-ttu-id="9a8f5-120">Если [**ID3DXInclude:: Open**](id3dxinclude--open.md) завершился успешно, метод **ID3DXInclude:: Close** гарантированно будет вызываться до того, как интерфейс API, использующий этот интерфейс, возвратит значение.</span><span class="sxs-lookup"><span data-stu-id="9a8f5-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a8f5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9a8f5-121">Requirements</span></span>



| <span data-ttu-id="9a8f5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9a8f5-122">Requirement</span></span> | <span data-ttu-id="9a8f5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9a8f5-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8f5-124">Header</span><span class="sxs-lookup"><span data-stu-id="9a8f5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9a8f5-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f5-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9a8f5-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a8f5-126">Library</span></span><br/> | <dl> <span data-ttu-id="9a8f5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a8f5-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9a8f5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a8f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a8f5-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="9a8f5-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="9a8f5-130">**ID3DXInclude:: Open**</span><span class="sxs-lookup"><span data-stu-id="9a8f5-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
