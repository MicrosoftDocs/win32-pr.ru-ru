---
title: Метод ID3DX11EffectSamplerVariable Ундосетсамплер (D3dx11effect. h)
description: Отменить ранее установленное состояние образца.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Метод Ундосетсамплер Direct3D 11
- Метод Ундосетсамплер Direct3D 11, интерфейс ID3DX11EffectSamplerVariable
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, метод Ундосетсамплер
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355760"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a><span data-ttu-id="95964-106">Метод ID3DX11EffectSamplerVariable:: Ундосетсамплер</span><span class="sxs-lookup"><span data-stu-id="95964-106">ID3DX11EffectSamplerVariable::UndoSetSampler method</span></span>

<span data-ttu-id="95964-107">Отменить ранее установленное состояние образца.</span><span class="sxs-lookup"><span data-stu-id="95964-107">Revert a previously set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="95964-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95964-108">Syntax</span></span>


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="95964-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="95964-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95964-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="95964-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="95964-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95964-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95964-112">Индекс в массиве интерфейсов образцов.</span><span class="sxs-lookup"><span data-stu-id="95964-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="95964-113">Если имеется только один интерфейс выборки, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="95964-113">If there is only one sampler interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95964-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95964-114">Return value</span></span>

<span data-ttu-id="95964-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95964-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95964-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="95964-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95964-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="95964-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95964-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="95964-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="95964-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="95964-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="95964-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="95964-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95964-121">Требования</span><span class="sxs-lookup"><span data-stu-id="95964-121">Requirements</span></span>



| <span data-ttu-id="95964-122">Требование</span><span class="sxs-lookup"><span data-stu-id="95964-122">Requirement</span></span> | <span data-ttu-id="95964-123">Значение</span><span class="sxs-lookup"><span data-stu-id="95964-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95964-124">Header</span><span class="sxs-lookup"><span data-stu-id="95964-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95964-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95964-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="95964-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95964-126">Library</span></span><br/> | <dl> <span data-ttu-id="95964-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="95964-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95964-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95964-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95964-129">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="95964-129">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

