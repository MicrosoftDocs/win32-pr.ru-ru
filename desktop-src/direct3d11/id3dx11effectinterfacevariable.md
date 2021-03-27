---
title: Интерфейс ID3DX11EffectInterfaceVariable (D3dx11effect. h)
description: Обращается к переменной интерфейса.
ms.assetid: c1d1f564-c7b8-4108-9988-972255662000
keywords:
- Интерфейс ID3DX11EffectInterfaceVariable Direct3D 11
- Интерфейс ID3DX11EffectInterfaceVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8169afc18e6974168e9196962b3e0cf87e860e4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986945"
---
# <a name="id3dx11effectinterfacevariable-interface"></a><span data-ttu-id="39dc2-105">Интерфейс ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="39dc2-105">ID3DX11EffectInterfaceVariable interface</span></span>

<span data-ttu-id="39dc2-106">Обращается к переменной интерфейса.</span><span class="sxs-lookup"><span data-stu-id="39dc2-106">Accesses an interface variable.</span></span>

## <a name="members"></a><span data-ttu-id="39dc2-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="39dc2-107">Members</span></span>

<span data-ttu-id="39dc2-108">Интерфейс **ID3DX11EffectInterfaceVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="39dc2-108">The **ID3DX11EffectInterfaceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="39dc2-109">**ID3DX11EffectInterfaceVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39dc2-109">**ID3DX11EffectInterfaceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="39dc2-110">Методы</span><span class="sxs-lookup"><span data-stu-id="39dc2-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="39dc2-111">Методы</span><span class="sxs-lookup"><span data-stu-id="39dc2-111">Methods</span></span>

<span data-ttu-id="39dc2-112">Интерфейс **ID3DX11EffectInterfaceVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="39dc2-112">The **ID3DX11EffectInterfaceVariable** interface has these methods.</span></span>



| <span data-ttu-id="39dc2-113">Метод</span><span class="sxs-lookup"><span data-stu-id="39dc2-113">Method</span></span>                                                                      | <span data-ttu-id="39dc2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="39dc2-114">Description</span></span>                       |
|:----------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="39dc2-115">**жетклассинстанце**</span><span class="sxs-lookup"><span data-stu-id="39dc2-115">**GetClassInstance**</span></span>](id3dx11effectinterfacevariable-getclassinstance.md) | <span data-ttu-id="39dc2-116">Получение экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="39dc2-116">Get a class instance.</span></span><br/>  |
| [<span data-ttu-id="39dc2-117">**сетклассинстанце**</span><span class="sxs-lookup"><span data-stu-id="39dc2-117">**SetClassInstance**</span></span>](id3dx11effectinterfacevariable-setclassinstance.md) | <span data-ttu-id="39dc2-118">Задает экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="39dc2-118">Sets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39dc2-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="39dc2-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="39dc2-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="39dc2-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="39dc2-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="39dc2-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="39dc2-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="39dc2-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39dc2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="39dc2-123">Requirements</span></span>



| <span data-ttu-id="39dc2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="39dc2-124">Requirement</span></span> | <span data-ttu-id="39dc2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="39dc2-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39dc2-126">Header</span><span class="sxs-lookup"><span data-stu-id="39dc2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="39dc2-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="39dc2-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="39dc2-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39dc2-128">Library</span></span><br/> | <dl> <span data-ttu-id="39dc2-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="39dc2-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39dc2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39dc2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39dc2-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="39dc2-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="39dc2-132">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="39dc2-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="39dc2-133">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="39dc2-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





