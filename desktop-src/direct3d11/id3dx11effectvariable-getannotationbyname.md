---
title: Метод ID3DX11EffectVariable Жетаннотатионбинаме (D3dx11effect. h)
description: Получение заметки по имени. | Метод ID3DX11EffectVariable Жетаннотатионбинаме (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Метод Жетаннотатионбинаме Direct3D 11
- Метод Жетаннотатионбинаме Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетаннотатионбинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355120"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a><span data-ttu-id="27a85-107">Метод ID3DX11EffectVariable:: Жетаннотатионбинаме</span><span class="sxs-lookup"><span data-stu-id="27a85-107">ID3DX11EffectVariable::GetAnnotationByName method</span></span>

<span data-ttu-id="27a85-108">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="27a85-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a85-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27a85-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="27a85-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="27a85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27a85-111">*имя*;</span><span class="sxs-lookup"><span data-stu-id="27a85-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="27a85-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="27a85-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="27a85-113">Имя заметки.</span><span class="sxs-lookup"><span data-stu-id="27a85-113">The annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27a85-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27a85-114">Return value</span></span>

<span data-ttu-id="27a85-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="27a85-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="27a85-116">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="27a85-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="27a85-117">Обратите внимание, что если заметка не найдена, возвращаемый **ID3DX11EffectVariable** будет пустым.</span><span class="sxs-lookup"><span data-stu-id="27a85-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="27a85-118">Чтобы определить, найдена ли заметка, следует вызвать метод [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="27a85-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="27a85-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="27a85-119">Remarks</span></span>

<span data-ttu-id="27a85-120">Аннонатионс можно подключить к методу, к Pass или к глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="27a85-120">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="27a85-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="27a85-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="27a85-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="27a85-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="27a85-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="27a85-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27a85-124">Требования</span><span class="sxs-lookup"><span data-stu-id="27a85-124">Requirements</span></span>



| <span data-ttu-id="27a85-125">Требование</span><span class="sxs-lookup"><span data-stu-id="27a85-125">Requirement</span></span> | <span data-ttu-id="27a85-126">Значение</span><span class="sxs-lookup"><span data-stu-id="27a85-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a85-127">Header</span><span class="sxs-lookup"><span data-stu-id="27a85-127">Header</span></span><br/>  | <dl> <span data-ttu-id="27a85-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="27a85-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="27a85-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27a85-129">Library</span></span><br/> | <dl> <span data-ttu-id="27a85-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="27a85-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27a85-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27a85-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a85-132">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="27a85-132">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

