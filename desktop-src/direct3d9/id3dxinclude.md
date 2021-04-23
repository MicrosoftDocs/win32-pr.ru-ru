---
description: ID3DXInclude — это реализованный пользователем интерфейс, обеспечивающий обратные вызовы для \# директив include во время компиляции шейдера.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Интерфейс ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703985"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="16914-103">Интерфейс ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="16914-103">ID3DXInclude interface</span></span>

<span data-ttu-id="16914-104">ID3DXInclude — это реализованный пользователем интерфейс, обеспечивающий обратные вызовы для \# директив include во время компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="16914-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="16914-105">Каждый из методов этого интерфейса должен быть реализован пользователем, который затем будет использоваться в качестве обратных вызовов приложения при возникновении одного из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="16914-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="16914-106">Шейдер HLSL, содержащий \# include, компилируется путем вызова одной из \* \* \* функций D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="16914-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="16914-107">Включение шейдера сборки \# осуществляется путем вызова любой из \* \* \* функций D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="16914-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="16914-108">Результат, содержащий include, \# компилируется путем вызова любой из \* \* \* функций D3DXCreateEffect или D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="16914-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="16914-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="16914-109">Members</span></span>

<span data-ttu-id="16914-110">Интерфейс **ID3DXInclude** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="16914-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="16914-111">**ID3DXInclude** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="16914-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="16914-112">Методы</span><span class="sxs-lookup"><span data-stu-id="16914-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16914-113">Методы</span><span class="sxs-lookup"><span data-stu-id="16914-113">Methods</span></span>

<span data-ttu-id="16914-114">Интерфейс **ID3DXInclude** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="16914-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="16914-115">Метод</span><span class="sxs-lookup"><span data-stu-id="16914-115">Method</span></span>                               | <span data-ttu-id="16914-116">Описание</span><span class="sxs-lookup"><span data-stu-id="16914-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16914-117">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="16914-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="16914-118">Реализованный пользователем метод для закрытия файла включения шейдера \# .</span><span class="sxs-lookup"><span data-stu-id="16914-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="16914-119">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="16914-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="16914-120">Реализованный пользователем метод для открытия и чтения содержимого \# включаемого файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="16914-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16914-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16914-121">Remarks</span></span>

<span data-ttu-id="16914-122">Пользователь создает интерфейс ID3DXInclude, реализуя класс, производный от этого интерфейса, и реализуя все методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="16914-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="16914-123">Тип LPD3DXINCLUDE определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="16914-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="16914-124">Требования</span><span class="sxs-lookup"><span data-stu-id="16914-124">Requirements</span></span>



| <span data-ttu-id="16914-125">Требование</span><span class="sxs-lookup"><span data-stu-id="16914-125">Requirement</span></span> | <span data-ttu-id="16914-126">Значение</span><span class="sxs-lookup"><span data-stu-id="16914-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16914-127">Header</span><span class="sxs-lookup"><span data-stu-id="16914-127">Header</span></span><br/>  | <dl> <span data-ttu-id="16914-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="16914-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="16914-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16914-129">Library</span></span><br/> | <dl> <span data-ttu-id="16914-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16914-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16914-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16914-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16914-132">Интерфейсы эффектов</span><span class="sxs-lookup"><span data-stu-id="16914-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
