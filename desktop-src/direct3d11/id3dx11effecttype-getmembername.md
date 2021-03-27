---
title: Метод ID3DX11EffectType Жетмембернаме (D3dx11effect. h)
description: Возвращает имя элемента.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Метод Жетмембернаме Direct3D 11
- Метод Жетмембернаме Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод Жетмембернаме
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355170"
---
# <a name="id3dx11effecttypegetmembername-method"></a><span data-ttu-id="53f3f-106">Метод ID3DX11EffectType:: Жетмембернаме</span><span class="sxs-lookup"><span data-stu-id="53f3f-106">ID3DX11EffectType::GetMemberName method</span></span>

<span data-ttu-id="53f3f-107">Возвращает имя элемента.</span><span class="sxs-lookup"><span data-stu-id="53f3f-107">Get the name of a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f3f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53f3f-108">Syntax</span></span>


```C++
LPCSTR GetMemberName(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="53f3f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="53f3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f3f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="53f3f-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="53f3f-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="53f3f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="53f3f-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="53f3f-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f3f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53f3f-113">Return value</span></span>

<span data-ttu-id="53f3f-114">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="53f3f-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="53f3f-115">Имя элемента.</span><span class="sxs-lookup"><span data-stu-id="53f3f-115">The name of the member.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f3f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="53f3f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53f3f-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="53f3f-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="53f3f-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="53f3f-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="53f3f-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="53f3f-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53f3f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="53f3f-120">Requirements</span></span>



| <span data-ttu-id="53f3f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="53f3f-121">Requirement</span></span> | <span data-ttu-id="53f3f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="53f3f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f3f-123">Header</span><span class="sxs-lookup"><span data-stu-id="53f3f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="53f3f-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f3f-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="53f3f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53f3f-125">Library</span></span><br/> | <dl> <span data-ttu-id="53f3f-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="53f3f-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f3f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53f3f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f3f-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="53f3f-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

