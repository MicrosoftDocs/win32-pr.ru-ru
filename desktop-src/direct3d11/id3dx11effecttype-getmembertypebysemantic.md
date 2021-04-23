---
title: Метод ID3DX11EffectType Жетмембертипебисемантик (D3dx11effect. h)
description: Получение типа члена по семантике.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Метод Жетмембертипебисемантик Direct3D 11
- Метод Жетмембертипебисемантик Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмембертипебисемантик
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5f0894c83ff2d0885ae3b951e0e324343fae8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998681"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a><span data-ttu-id="06a33-106">Метод ID3DX11EffectType:: Жетмембертипебисемантик</span><span class="sxs-lookup"><span data-stu-id="06a33-106">ID3DX11EffectType::GetMemberTypeBySemantic method</span></span>

<span data-ttu-id="06a33-107">Получение типа члена по семантике.</span><span class="sxs-lookup"><span data-stu-id="06a33-107">Get a member type by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a33-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06a33-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="06a33-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="06a33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a33-110">*Семантическ*</span><span class="sxs-lookup"><span data-stu-id="06a33-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="06a33-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06a33-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="06a33-112">Семантика.</span><span class="sxs-lookup"><span data-stu-id="06a33-112">A semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a33-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06a33-113">Return value</span></span>

<span data-ttu-id="06a33-114">Тип: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="06a33-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="06a33-115">Указатель на [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="06a33-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06a33-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="06a33-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06a33-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="06a33-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="06a33-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="06a33-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="06a33-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="06a33-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06a33-120">Требования</span><span class="sxs-lookup"><span data-stu-id="06a33-120">Requirements</span></span>



| <span data-ttu-id="06a33-121">Требование</span><span class="sxs-lookup"><span data-stu-id="06a33-121">Requirement</span></span> | <span data-ttu-id="06a33-122">Значение</span><span class="sxs-lookup"><span data-stu-id="06a33-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a33-123">Header</span><span class="sxs-lookup"><span data-stu-id="06a33-123">Header</span></span><br/>  | <dl> <span data-ttu-id="06a33-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a33-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="06a33-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06a33-125">Library</span></span><br/> | <dl> <span data-ttu-id="06a33-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="06a33-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a33-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06a33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a33-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="06a33-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

