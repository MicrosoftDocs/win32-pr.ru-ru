---
title: Метод ID3DX11EffectType Жетмембертипебиндекс (D3dx11effect. h)
description: Получение типа элемента по индексу.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Метод Жетмембертипебиндекс Direct3D 11
- Метод Жетмембертипебиндекс Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмембертипебиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547983"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="9ed59-106">Метод ID3DX11EffectType:: Жетмембертипебиндекс</span><span class="sxs-lookup"><span data-stu-id="9ed59-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="9ed59-107">Получение типа элемента по индексу.</span><span class="sxs-lookup"><span data-stu-id="9ed59-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed59-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ed59-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="9ed59-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ed59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed59-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9ed59-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed59-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9ed59-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9ed59-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="9ed59-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed59-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ed59-113">Return value</span></span>

<span data-ttu-id="9ed59-114">Тип: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed59-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="9ed59-115">Указатель на [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="9ed59-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed59-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ed59-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ed59-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9ed59-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9ed59-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9ed59-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9ed59-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9ed59-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ed59-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9ed59-120">Requirements</span></span>



| <span data-ttu-id="9ed59-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9ed59-121">Requirement</span></span> | <span data-ttu-id="9ed59-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9ed59-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed59-123">Header</span><span class="sxs-lookup"><span data-stu-id="9ed59-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9ed59-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed59-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9ed59-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ed59-125">Library</span></span><br/> | <dl> <span data-ttu-id="9ed59-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed59-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed59-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ed59-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed59-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="9ed59-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

