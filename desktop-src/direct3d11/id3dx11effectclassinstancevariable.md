---
title: Интерфейс ID3DX11EffectClassInstanceVariable (D3dx11effect. h)
description: Обращается к экземпляру класса.
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- Интерфейс ID3DX11EffectClassInstanceVariable Direct3D 11
- Интерфейс ID3DX11EffectClassInstanceVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355983"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="548f0-105">Интерфейс ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="548f0-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="548f0-106">Обращается к экземпляру класса.</span><span class="sxs-lookup"><span data-stu-id="548f0-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="548f0-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="548f0-107">Members</span></span>

<span data-ttu-id="548f0-108">Интерфейс **ID3DX11EffectClassInstanceVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="548f0-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="548f0-109">**ID3DX11EffectClassInstanceVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="548f0-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="548f0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="548f0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="548f0-111">Методы</span><span class="sxs-lookup"><span data-stu-id="548f0-111">Methods</span></span>

<span data-ttu-id="548f0-112">Интерфейс **ID3DX11EffectClassInstanceVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="548f0-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="548f0-113">Метод</span><span class="sxs-lookup"><span data-stu-id="548f0-113">Method</span></span>                                                                          | <span data-ttu-id="548f0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="548f0-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="548f0-115">**жетклассинстанце**</span><span class="sxs-lookup"><span data-stu-id="548f0-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="548f0-116">Возвращает экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="548f0-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="548f0-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="548f0-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="548f0-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="548f0-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="548f0-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="548f0-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="548f0-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="548f0-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="548f0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="548f0-121">Requirements</span></span>



| <span data-ttu-id="548f0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="548f0-122">Requirement</span></span> | <span data-ttu-id="548f0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="548f0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="548f0-124">Header</span><span class="sxs-lookup"><span data-stu-id="548f0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="548f0-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="548f0-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="548f0-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="548f0-126">Library</span></span><br/> | <dl> <span data-ttu-id="548f0-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="548f0-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548f0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="548f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548f0-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="548f0-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="548f0-130">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="548f0-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="548f0-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="548f0-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





