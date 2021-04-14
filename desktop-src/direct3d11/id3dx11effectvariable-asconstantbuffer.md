---
title: Метод ID3DX11EffectVariable Асконстантбуффер (D3dx11effect. h)
description: Получение буфера константы. | Метод ID3DX11EffectVariable Асконстантбуффер (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Метод Асконстантбуффер Direct3D 11
- Метод Асконстантбуффер Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998432"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a><span data-ttu-id="c02cd-107">Метод ID3DX11EffectVariable:: Асконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="c02cd-107">ID3DX11EffectVariable::AsConstantBuffer method</span></span>

<span data-ttu-id="c02cd-108">Получение буфера константы.</span><span class="sxs-lookup"><span data-stu-id="c02cd-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c02cd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c02cd-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="c02cd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c02cd-110">Parameters</span></span>

<span data-ttu-id="c02cd-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c02cd-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c02cd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c02cd-112">Return value</span></span>

<span data-ttu-id="c02cd-113">Тип: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c02cd-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="c02cd-114">Указатель на буфер константы.</span><span class="sxs-lookup"><span data-stu-id="c02cd-114">A pointer to a constant buffer.</span></span> <span data-ttu-id="c02cd-115">См. [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c02cd-115">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c02cd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c02cd-116">Remarks</span></span>

<span data-ttu-id="c02cd-117">Асконстантбуффер Возвращает версию переменной Effect, которая была специализированной для буфера констант.</span><span class="sxs-lookup"><span data-stu-id="c02cd-117">AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer.</span></span> <span data-ttu-id="c02cd-118">Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данные буфера констант.</span><span class="sxs-lookup"><span data-stu-id="c02cd-118">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.</span></span>

<span data-ttu-id="c02cd-119">Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="c02cd-119">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="c02cd-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c02cd-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c02cd-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c02cd-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c02cd-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c02cd-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c02cd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c02cd-123">Requirements</span></span>



| <span data-ttu-id="c02cd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c02cd-124">Requirement</span></span> | <span data-ttu-id="c02cd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c02cd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02cd-126">Header</span><span class="sxs-lookup"><span data-stu-id="c02cd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c02cd-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02cd-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c02cd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c02cd-128">Library</span></span><br/> | <dl> <span data-ttu-id="c02cd-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c02cd-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c02cd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c02cd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02cd-131">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c02cd-131">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





