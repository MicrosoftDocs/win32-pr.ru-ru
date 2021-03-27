---
title: Метод ID3DX11Effect Клониффект (D3dx11effect. h)
description: Создает копию интерфейса Effect.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Метод Клониффект Direct3D 11
- Метод Клониффект Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Клониффект
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987242"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="49542-106">Метод ID3DX11Effect:: Клониффект</span><span class="sxs-lookup"><span data-stu-id="49542-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="49542-107">Создает копию интерфейса Effect.</span><span class="sxs-lookup"><span data-stu-id="49542-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="49542-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49542-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="49542-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49542-110">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="49542-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="49542-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49542-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="49542-112">Флаги, влияющие на создание клонированного результата.</span><span class="sxs-lookup"><span data-stu-id="49542-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="49542-113">Может иметь значение 0 или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="49542-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="49542-114">Flag</span><span class="sxs-lookup"><span data-stu-id="49542-114">Flag</span></span>                                    | <span data-ttu-id="49542-115">Описание</span><span class="sxs-lookup"><span data-stu-id="49542-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49542-116">D3DX11 \_ воздействие \_ клона в \_ \_ неодном</span><span class="sxs-lookup"><span data-stu-id="49542-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="49542-117">Игнорировать все "одиночные" квалификаторы в cbuffer.</span><span class="sxs-lookup"><span data-stu-id="49542-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="49542-118">Все cbuffer будут иметь собственные [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s, созданные в клонированном результате.</span><span class="sxs-lookup"><span data-stu-id="49542-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="49542-119">*ппклонедеффект*</span><span class="sxs-lookup"><span data-stu-id="49542-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="49542-120">Тип: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="49542-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="49542-121">Указатель на указатель [**ID3DX11Effect**](id3dx11effect.md) , который будет установлен в копию результата.</span><span class="sxs-lookup"><span data-stu-id="49542-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49542-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49542-122">Return value</span></span>

<span data-ttu-id="49542-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49542-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49542-124">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="49542-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49542-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="49542-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49542-126">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="49542-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="49542-127">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="49542-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="49542-128">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="49542-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49542-129">Требования</span><span class="sxs-lookup"><span data-stu-id="49542-129">Requirements</span></span>



| <span data-ttu-id="49542-130">Требование</span><span class="sxs-lookup"><span data-stu-id="49542-130">Requirement</span></span> | <span data-ttu-id="49542-131">Значение</span><span class="sxs-lookup"><span data-stu-id="49542-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49542-132">Header</span><span class="sxs-lookup"><span data-stu-id="49542-132">Header</span></span><br/>  | <dl> <span data-ttu-id="49542-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="49542-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="49542-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49542-134">Library</span></span><br/> | <dl> <span data-ttu-id="49542-135"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="49542-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49542-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49542-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49542-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="49542-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

