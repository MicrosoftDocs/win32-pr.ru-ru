---
title: Метод ID3DX11EffectVariable Асклассинстанце (D3dx11effect. h)
description: Получение переменной экземпляра класса.
ms.assetid: c1d4adb5-7cd2-4ba2-9a91-3d03f9596a10
keywords:
- Метод Асклассинстанце Direct3D 11
- Метод Асклассинстанце Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17dc9124f4b9a24ead503694c10a4a2d2205ed3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998321"
---
# <a name="id3dx11effectvariableasclassinstance-method"></a><span data-ttu-id="b5b03-106">Метод ID3DX11EffectVariable:: Асклассинстанце</span><span class="sxs-lookup"><span data-stu-id="b5b03-106">ID3DX11EffectVariable::AsClassInstance method</span></span>

<span data-ttu-id="b5b03-107">Получение переменной экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="b5b03-107">Get a class-instance variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b03-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5b03-108">Syntax</span></span>


```C++
ID3DX11EffectClassInstanceVariable* AsClassInstance();
```



## <a name="parameters"></a><span data-ttu-id="b5b03-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5b03-109">Parameters</span></span>

<span data-ttu-id="b5b03-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b5b03-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5b03-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5b03-111">Return value</span></span>

<span data-ttu-id="b5b03-112">Тип: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5b03-112">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="b5b03-113">Указатель на переменную экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="b5b03-113">A pointer to class-instance variable.</span></span> <span data-ttu-id="b5b03-114">См. [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span><span class="sxs-lookup"><span data-stu-id="b5b03-114">See [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b03-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5b03-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5b03-116">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="b5b03-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b5b03-117">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="b5b03-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b5b03-118">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b5b03-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5b03-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b5b03-119">Requirements</span></span>



| <span data-ttu-id="b5b03-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b5b03-120">Requirement</span></span> | <span data-ttu-id="b5b03-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b5b03-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b03-122">Header</span><span class="sxs-lookup"><span data-stu-id="b5b03-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b5b03-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5b03-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b5b03-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5b03-124">Library</span></span><br/> | <dl> <span data-ttu-id="b5b03-125"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="b5b03-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b03-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5b03-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b03-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="b5b03-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





