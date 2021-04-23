---
title: Метод ID3DX11EffectVariable Жетмембербисемантик (D3dx11effect. h)
description: Получение члена структуры по семантике.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Метод Жетмембербисемантик Direct3D 11
- Метод Жетмембербисемантик Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетмембербисемантик
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998702"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a><span data-ttu-id="92ff4-106">Метод ID3DX11EffectVariable:: Жетмембербисемантик</span><span class="sxs-lookup"><span data-stu-id="92ff4-106">ID3DX11EffectVariable::GetMemberBySemantic method</span></span>

<span data-ttu-id="92ff4-107">Получение члена структуры по семантике.</span><span class="sxs-lookup"><span data-stu-id="92ff4-107">Get a structure member by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="92ff4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92ff4-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="92ff4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92ff4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92ff4-110">*Семантическ*</span><span class="sxs-lookup"><span data-stu-id="92ff4-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="92ff4-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92ff4-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92ff4-112">Семантика.</span><span class="sxs-lookup"><span data-stu-id="92ff4-112">The semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92ff4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92ff4-113">Return value</span></span>

<span data-ttu-id="92ff4-114">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="92ff4-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="92ff4-115">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="92ff4-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92ff4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="92ff4-116">Remarks</span></span>

<span data-ttu-id="92ff4-117">Если переменная действия является структурой, используйте этот метод для поиска члена по присоединенной семантике.</span><span class="sxs-lookup"><span data-stu-id="92ff4-117">If the effect variable is an structure, use this method to look up a member by attached semantic.</span></span>

> [!Note]  
> <span data-ttu-id="92ff4-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="92ff4-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="92ff4-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="92ff4-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="92ff4-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="92ff4-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92ff4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="92ff4-121">Requirements</span></span>



| <span data-ttu-id="92ff4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="92ff4-122">Requirement</span></span> | <span data-ttu-id="92ff4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="92ff4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ff4-124">Header</span><span class="sxs-lookup"><span data-stu-id="92ff4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="92ff4-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ff4-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="92ff4-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92ff4-126">Library</span></span><br/> | <dl> <span data-ttu-id="92ff4-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="92ff4-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ff4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92ff4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ff4-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="92ff4-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

