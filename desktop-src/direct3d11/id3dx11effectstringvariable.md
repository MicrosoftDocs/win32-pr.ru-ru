---
title: Интерфейс ID3DX11EffectStringVariable (D3dx11effect. h)
description: Интерфейс строковых переменных обращается к строковой переменной.
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- Интерфейс ID3DX11EffectStringVariable Direct3D 11
- Интерфейс ID3DX11EffectStringVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998324"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="fe216-105">Интерфейс ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="fe216-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="fe216-106">Интерфейс строковых переменных обращается к строковой переменной.</span><span class="sxs-lookup"><span data-stu-id="fe216-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="fe216-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="fe216-107">Members</span></span>

<span data-ttu-id="fe216-108">Интерфейс **ID3DX11EffectStringVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="fe216-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="fe216-109">**ID3DX11EffectStringVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fe216-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="fe216-110">Методы</span><span class="sxs-lookup"><span data-stu-id="fe216-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe216-111">Методы</span><span class="sxs-lookup"><span data-stu-id="fe216-111">Methods</span></span>

<span data-ttu-id="fe216-112">Интерфейс **ID3DX11EffectStringVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fe216-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="fe216-113">Метод</span><span class="sxs-lookup"><span data-stu-id="fe216-113">Method</span></span>                                                               | <span data-ttu-id="fe216-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fe216-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="fe216-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="fe216-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="fe216-116">Получите строку.</span><span class="sxs-lookup"><span data-stu-id="fe216-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="fe216-117">**жетстрингаррай**</span><span class="sxs-lookup"><span data-stu-id="fe216-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="fe216-118">Получение массива строк.</span><span class="sxs-lookup"><span data-stu-id="fe216-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe216-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe216-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe216-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="fe216-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fe216-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="fe216-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fe216-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fe216-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe216-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fe216-123">Requirements</span></span>



| <span data-ttu-id="fe216-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fe216-124">Requirement</span></span> | <span data-ttu-id="fe216-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fe216-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe216-126">Header</span><span class="sxs-lookup"><span data-stu-id="fe216-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fe216-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe216-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fe216-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe216-128">Library</span></span><br/> | <dl> <span data-ttu-id="fe216-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="fe216-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe216-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe216-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe216-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="fe216-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="fe216-132">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="fe216-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fe216-133">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="fe216-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





