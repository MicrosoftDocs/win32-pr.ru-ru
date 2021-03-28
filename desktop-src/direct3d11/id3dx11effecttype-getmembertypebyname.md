---
title: Метод ID3DX11EffectType Жетмембертипебинаме (D3dx11effect. h)
description: Получение типа элемента по имени.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Метод Жетмембертипебинаме Direct3D 11
- Метод Жетмембертипебинаме Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмембертипебинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998366"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a><span data-ttu-id="92399-106">Метод ID3DX11EffectType:: Жетмембертипебинаме</span><span class="sxs-lookup"><span data-stu-id="92399-106">ID3DX11EffectType::GetMemberTypeByName method</span></span>

<span data-ttu-id="92399-107">Получение типа элемента по имени.</span><span class="sxs-lookup"><span data-stu-id="92399-107">Get an member type by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="92399-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92399-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="92399-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92399-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92399-110">*имя*;</span><span class="sxs-lookup"><span data-stu-id="92399-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="92399-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92399-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92399-112">Имя члена.</span><span class="sxs-lookup"><span data-stu-id="92399-112">A member's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92399-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92399-113">Return value</span></span>

<span data-ttu-id="92399-114">Тип: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="92399-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="92399-115">Указатель на [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="92399-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92399-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="92399-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="92399-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="92399-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="92399-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="92399-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="92399-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="92399-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92399-120">Требования</span><span class="sxs-lookup"><span data-stu-id="92399-120">Requirements</span></span>



| <span data-ttu-id="92399-121">Требование</span><span class="sxs-lookup"><span data-stu-id="92399-121">Requirement</span></span> | <span data-ttu-id="92399-122">Значение</span><span class="sxs-lookup"><span data-stu-id="92399-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92399-123">Header</span><span class="sxs-lookup"><span data-stu-id="92399-123">Header</span></span><br/>  | <dl> <span data-ttu-id="92399-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="92399-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="92399-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92399-125">Library</span></span><br/> | <dl> <span data-ttu-id="92399-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="92399-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92399-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92399-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92399-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="92399-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

