---
title: Метод ID3DX11EffectVariable-desc (D3dx11effect. h)
description: Получить описание.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11EffectVariable
- ID3DX11EffectVariable интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625b9d72b3ff4afe1880b48125d244da1f68844
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998753"
---
# <a name="id3dx11effectvariablegetdesc-method"></a><span data-ttu-id="816ac-106">Метод ID3DX11EffectVariable:: DESC</span><span class="sxs-lookup"><span data-stu-id="816ac-106">ID3DX11EffectVariable::GetDesc method</span></span>

<span data-ttu-id="816ac-107">Получить описание.</span><span class="sxs-lookup"><span data-stu-id="816ac-107">Get a description.</span></span>

## <a name="syntax"></a><span data-ttu-id="816ac-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="816ac-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="816ac-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="816ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="816ac-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="816ac-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="816ac-111">Тип: **[ **D3DX11 \_ результат \_ переменная \_ DESC**](d3dx11-effect-variable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="816ac-111">Type: **[**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)\***</span></span>

<span data-ttu-id="816ac-112">Указатель на описание переменной Effect (см. [**D3DX11 \_ Effect \_ переменная \_ DESC**](d3dx11-effect-variable-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="816ac-112">A pointer to an effect-variable description (see [**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="816ac-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="816ac-113">Return value</span></span>

<span data-ttu-id="816ac-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="816ac-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="816ac-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="816ac-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="816ac-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="816ac-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="816ac-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="816ac-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="816ac-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="816ac-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="816ac-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="816ac-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="816ac-120">Требования</span><span class="sxs-lookup"><span data-stu-id="816ac-120">Requirements</span></span>



| <span data-ttu-id="816ac-121">Требование</span><span class="sxs-lookup"><span data-stu-id="816ac-121">Requirement</span></span> | <span data-ttu-id="816ac-122">Значение</span><span class="sxs-lookup"><span data-stu-id="816ac-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="816ac-123">Header</span><span class="sxs-lookup"><span data-stu-id="816ac-123">Header</span></span><br/>  | <dl> <span data-ttu-id="816ac-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="816ac-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="816ac-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="816ac-125">Library</span></span><br/> | <dl> <span data-ttu-id="816ac-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="816ac-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="816ac-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="816ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816ac-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="816ac-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





