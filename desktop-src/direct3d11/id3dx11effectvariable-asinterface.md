---
title: Метод ID3DX11EffectVariable Асинтерфаце (D3dx11effect. h)
description: Возвращает переменную интерфейса.
ms.assetid: 5b1e5d05-ab36-42c2-9990-154baff5e9a4
keywords:
- Метод Асинтерфаце Direct3D 11
- Метод Асинтерфаце Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асинтерфаце
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsInterface
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0134aceea3202e0965bf05b709d29279be2fc29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820940"
---
# <a name="id3dx11effectvariableasinterface-method"></a><span data-ttu-id="23c4e-106">Метод ID3DX11EffectVariable:: Асинтерфаце</span><span class="sxs-lookup"><span data-stu-id="23c4e-106">ID3DX11EffectVariable::AsInterface method</span></span>

<span data-ttu-id="23c4e-107">Возвращает переменную интерфейса.</span><span class="sxs-lookup"><span data-stu-id="23c4e-107">Get an interface variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c4e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23c4e-108">Syntax</span></span>


```C++
ID3DX11EffectInterfaceVariable* AsInterface();
```



## <a name="parameters"></a><span data-ttu-id="23c4e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="23c4e-109">Parameters</span></span>

<span data-ttu-id="23c4e-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="23c4e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23c4e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23c4e-111">Return value</span></span>

<span data-ttu-id="23c4e-112">Тип: **[ **ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="23c4e-112">Type: **[**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span></span>

<span data-ttu-id="23c4e-113">Указатель на переменную интерфейса.</span><span class="sxs-lookup"><span data-stu-id="23c4e-113">A pointer to an interface variable.</span></span> <span data-ttu-id="23c4e-114">См. [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span><span class="sxs-lookup"><span data-stu-id="23c4e-114">See [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23c4e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="23c4e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23c4e-116">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="23c4e-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23c4e-117">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="23c4e-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23c4e-118">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="23c4e-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23c4e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="23c4e-119">Requirements</span></span>



| <span data-ttu-id="23c4e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="23c4e-120">Requirement</span></span> | <span data-ttu-id="23c4e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="23c4e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c4e-122">Header</span><span class="sxs-lookup"><span data-stu-id="23c4e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="23c4e-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c4e-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23c4e-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23c4e-124">Library</span></span><br/> | <dl> <span data-ttu-id="23c4e-125"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="23c4e-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c4e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23c4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c4e-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="23c4e-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





