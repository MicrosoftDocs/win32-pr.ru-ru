---
title: Метод ID3DX11EffectType Жетмемберсемантик (D3dx11effect. h)
description: Возвращает семантическую присоединение к элементу.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Метод Жетмемберсемантик Direct3D 11
- Метод Жетмемберсемантик Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмемберсемантик
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998384"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a><span data-ttu-id="24230-106">Метод ID3DX11EffectType:: Жетмемберсемантик</span><span class="sxs-lookup"><span data-stu-id="24230-106">ID3DX11EffectType::GetMemberSemantic method</span></span>

<span data-ttu-id="24230-107">Возвращает семантическую присоединение к элементу.</span><span class="sxs-lookup"><span data-stu-id="24230-107">Get the semantic attached to a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="24230-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24230-108">Syntax</span></span>


```C++
LPCSTR GetMemberSemantic(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="24230-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="24230-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24230-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="24230-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="24230-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24230-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24230-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="24230-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24230-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24230-113">Return value</span></span>

<span data-ttu-id="24230-114">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24230-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24230-115">Строка, содержащая семантику.</span><span class="sxs-lookup"><span data-stu-id="24230-115">A string that contains the semantic.</span></span>

## <a name="remarks"></a><span data-ttu-id="24230-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="24230-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24230-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="24230-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="24230-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="24230-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="24230-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="24230-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24230-120">Требования</span><span class="sxs-lookup"><span data-stu-id="24230-120">Requirements</span></span>



| <span data-ttu-id="24230-121">Требование</span><span class="sxs-lookup"><span data-stu-id="24230-121">Requirement</span></span> | <span data-ttu-id="24230-122">Значение</span><span class="sxs-lookup"><span data-stu-id="24230-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24230-123">Header</span><span class="sxs-lookup"><span data-stu-id="24230-123">Header</span></span><br/>  | <dl> <span data-ttu-id="24230-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="24230-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="24230-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24230-125">Library</span></span><br/> | <dl> <span data-ttu-id="24230-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="24230-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24230-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24230-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24230-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="24230-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

