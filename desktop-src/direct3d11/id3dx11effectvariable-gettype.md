---
title: Метод GetType ID3DX11EffectVariable (D3dx11effect. h)
description: Получение сведений о типе.
ms.assetid: c9ada96a-0259-48c1-b869-ba0f51bf4600
keywords:
- Метод GetType Direct3D 11
- Метод GetType Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод GetType
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a6a654dd815770da8913660b22215dfbecc36b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354243"
---
# <a name="id3dx11effectvariablegettype-method"></a><span data-ttu-id="0ca65-106">Метод ID3DX11EffectVariable:: GetType</span><span class="sxs-lookup"><span data-stu-id="0ca65-106">ID3DX11EffectVariable::GetType method</span></span>

<span data-ttu-id="0ca65-107">Получение сведений о типе.</span><span class="sxs-lookup"><span data-stu-id="0ca65-107">Get type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca65-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ca65-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetType();
```



## <a name="parameters"></a><span data-ttu-id="0ca65-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ca65-109">Parameters</span></span>

<span data-ttu-id="0ca65-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ca65-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ca65-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ca65-111">Return value</span></span>

<span data-ttu-id="0ca65-112">Тип: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ca65-112">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="0ca65-113">Указатель на [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="0ca65-113">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca65-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ca65-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ca65-115">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="0ca65-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0ca65-116">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="0ca65-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0ca65-117">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0ca65-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ca65-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0ca65-118">Requirements</span></span>



| <span data-ttu-id="0ca65-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0ca65-119">Requirement</span></span> | <span data-ttu-id="0ca65-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0ca65-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca65-121">Header</span><span class="sxs-lookup"><span data-stu-id="0ca65-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0ca65-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca65-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0ca65-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ca65-123">Library</span></span><br/> | <dl> <span data-ttu-id="0ca65-124"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="0ca65-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca65-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ca65-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca65-126">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="0ca65-126">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





