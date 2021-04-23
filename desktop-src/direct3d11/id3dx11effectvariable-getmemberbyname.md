---
title: Метод ID3DX11EffectVariable Жетмембербинаме (D3dx11effect. h)
description: Получение члена структуры по имени.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Метод Жетмембербинаме Direct3D 11
- Метод Жетмембербинаме Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетмембербинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998750"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a><span data-ttu-id="cc5fb-106">Метод ID3DX11EffectVariable:: Жетмембербинаме</span><span class="sxs-lookup"><span data-stu-id="cc5fb-106">ID3DX11EffectVariable::GetMemberByName method</span></span>

<span data-ttu-id="cc5fb-107">Получение члена структуры по имени.</span><span class="sxs-lookup"><span data-stu-id="cc5fb-107">Get a structure member by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5fb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc5fb-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="cc5fb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc5fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc5fb-110">*имя*;</span><span class="sxs-lookup"><span data-stu-id="cc5fb-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="cc5fb-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc5fb-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc5fb-112">Имя члена.</span><span class="sxs-lookup"><span data-stu-id="cc5fb-112">Member name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc5fb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc5fb-113">Return value</span></span>

<span data-ttu-id="cc5fb-114">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc5fb-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="cc5fb-115">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="cc5fb-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc5fb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc5fb-116">Remarks</span></span>

<span data-ttu-id="cc5fb-117">Если переменная действия является структурой, используйте этот метод для поиска элемента по имени.</span><span class="sxs-lookup"><span data-stu-id="cc5fb-117">If the effect variable is an structure, use this method to look up a member by name.</span></span>

> [!Note]  
> <span data-ttu-id="cc5fb-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="cc5fb-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cc5fb-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="cc5fb-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cc5fb-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cc5fb-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc5fb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cc5fb-121">Requirements</span></span>



| <span data-ttu-id="cc5fb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cc5fb-122">Requirement</span></span> | <span data-ttu-id="cc5fb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cc5fb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5fb-124">Header</span><span class="sxs-lookup"><span data-stu-id="cc5fb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cc5fb-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc5fb-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cc5fb-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc5fb-126">Library</span></span><br/> | <dl> <span data-ttu-id="cc5fb-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="cc5fb-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc5fb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc5fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc5fb-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cc5fb-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

