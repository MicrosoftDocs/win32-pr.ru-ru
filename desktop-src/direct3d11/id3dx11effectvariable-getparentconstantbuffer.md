---
title: Метод ID3DX11EffectVariable Жетпарентконстантбуффер (D3dx11effect. h)
description: Получение буфера константы. | Метод ID3DX11EffectVariable Жетпарентконстантбуффер (D3dx11effect. h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Метод Жетпарентконстантбуффер Direct3D 11
- Метод Жетпарентконстантбуффер Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетпарентконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa424b91b72dca5539fd0f96a1380e86d1f23f58
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998726"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a><span data-ttu-id="f6122-107">Метод ID3DX11EffectVariable:: Жетпарентконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="f6122-107">ID3DX11EffectVariable::GetParentConstantBuffer method</span></span>

<span data-ttu-id="f6122-108">Получение буфера константы.</span><span class="sxs-lookup"><span data-stu-id="f6122-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6122-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6122-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="f6122-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6122-110">Parameters</span></span>

<span data-ttu-id="f6122-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f6122-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6122-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6122-112">Return value</span></span>

<span data-ttu-id="f6122-113">Тип: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6122-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="f6122-114">Указатель на [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f6122-114">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6122-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6122-115">Remarks</span></span>

<span data-ttu-id="f6122-116">Переменные эффектов считываются или записываются в буфер констант.</span><span class="sxs-lookup"><span data-stu-id="f6122-116">Effect variables are read-from or written-to a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="f6122-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="f6122-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f6122-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="f6122-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f6122-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f6122-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6122-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f6122-120">Requirements</span></span>



| <span data-ttu-id="f6122-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f6122-121">Requirement</span></span> | <span data-ttu-id="f6122-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f6122-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6122-123">Header</span><span class="sxs-lookup"><span data-stu-id="f6122-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f6122-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6122-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f6122-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6122-125">Library</span></span><br/> | <dl> <span data-ttu-id="f6122-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="f6122-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6122-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6122-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6122-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f6122-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





