---
title: Метод ID3DX11Effect Жетграупбинаме (D3dx11effect. h)
description: Возвращает группу эффектов по имени.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Метод Жетграупбинаме Direct3D 11
- Метод Жетграупбинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетграупбинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998627"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="f463a-106">Метод ID3DX11Effect:: Жетграупбинаме</span><span class="sxs-lookup"><span data-stu-id="f463a-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="f463a-107">Возвращает группу эффектов по имени.</span><span class="sxs-lookup"><span data-stu-id="f463a-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f463a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f463a-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="f463a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f463a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f463a-110">*имя*;</span><span class="sxs-lookup"><span data-stu-id="f463a-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="f463a-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f463a-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f463a-112">Имя группы эффектов.</span><span class="sxs-lookup"><span data-stu-id="f463a-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f463a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f463a-113">Return value</span></span>

<span data-ttu-id="f463a-114">Тип: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="f463a-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="f463a-115">Указатель на интерфейс [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="f463a-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="f463a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f463a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f463a-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="f463a-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f463a-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="f463a-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f463a-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f463a-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f463a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f463a-120">Requirements</span></span>



| <span data-ttu-id="f463a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f463a-121">Requirement</span></span> | <span data-ttu-id="f463a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f463a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f463a-123">Header</span><span class="sxs-lookup"><span data-stu-id="f463a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f463a-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f463a-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f463a-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f463a-125">Library</span></span><br/> | <dl> <span data-ttu-id="f463a-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="f463a-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f463a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f463a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f463a-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="f463a-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

