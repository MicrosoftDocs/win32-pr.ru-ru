---
title: Интерфейс ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Интерфейс постоянного буфера обращается к постоянным буферам или буферам текстур.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355253"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="691c7-105">Интерфейс ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="691c7-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="691c7-106">Интерфейс постоянного буфера обращается к постоянным буферам или буферам текстур.</span><span class="sxs-lookup"><span data-stu-id="691c7-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="691c7-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="691c7-107">Members</span></span>

<span data-ttu-id="691c7-108">Интерфейс **ID3DX11EffectConstantBuffer** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="691c7-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="691c7-109">**ID3DX11EffectConstantBuffer** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="691c7-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="691c7-110">Методы</span><span class="sxs-lookup"><span data-stu-id="691c7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="691c7-111">Методы</span><span class="sxs-lookup"><span data-stu-id="691c7-111">Methods</span></span>

<span data-ttu-id="691c7-112">Интерфейс **ID3DX11EffectConstantBuffer** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="691c7-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="691c7-113">Метод</span><span class="sxs-lookup"><span data-stu-id="691c7-113">Method</span></span>                                                                             | <span data-ttu-id="691c7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="691c7-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="691c7-115">**жетконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="691c7-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="691c7-116">Получение постоянного буфера.</span><span class="sxs-lookup"><span data-stu-id="691c7-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="691c7-117">**жеттекстуребуффер**</span><span class="sxs-lookup"><span data-stu-id="691c7-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="691c7-118">Получение буфера текстуры.</span><span class="sxs-lookup"><span data-stu-id="691c7-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="691c7-119">**сетконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="691c7-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="691c7-120">Установите константный буфер.</span><span class="sxs-lookup"><span data-stu-id="691c7-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="691c7-121">**сеттекстуребуффер**</span><span class="sxs-lookup"><span data-stu-id="691c7-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="691c7-122">Задайте буфер текстуры.</span><span class="sxs-lookup"><span data-stu-id="691c7-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="691c7-123">**ундосетконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="691c7-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="691c7-124">Восстанавливает ранее установленный буфер констант.</span><span class="sxs-lookup"><span data-stu-id="691c7-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="691c7-125">**ундосеттекстуребуффер**</span><span class="sxs-lookup"><span data-stu-id="691c7-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="691c7-126">Восстанавливает ранее установленный буфер текстуры.</span><span class="sxs-lookup"><span data-stu-id="691c7-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="691c7-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="691c7-127">Remarks</span></span>

<span data-ttu-id="691c7-128">Используйте буферы констант для хранения многих констант эффектов; Группирование констант в буферы на основе частоты обновления.</span><span class="sxs-lookup"><span data-stu-id="691c7-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="691c7-129">Это позволяет максимально сокращать количество изменений состояния, а также упростить изменение состояния минимальных вызовов API.</span><span class="sxs-lookup"><span data-stu-id="691c7-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="691c7-130">Оба эти фактора приводят к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="691c7-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="691c7-131">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="691c7-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="691c7-132">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="691c7-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="691c7-133">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="691c7-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="691c7-134">Требования</span><span class="sxs-lookup"><span data-stu-id="691c7-134">Requirements</span></span>



| <span data-ttu-id="691c7-135">Требование</span><span class="sxs-lookup"><span data-stu-id="691c7-135">Requirement</span></span> | <span data-ttu-id="691c7-136">Значение</span><span class="sxs-lookup"><span data-stu-id="691c7-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="691c7-137">Header</span><span class="sxs-lookup"><span data-stu-id="691c7-137">Header</span></span><br/>  | <dl> <span data-ttu-id="691c7-138"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="691c7-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="691c7-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="691c7-139">Library</span></span><br/> | <dl> <span data-ttu-id="691c7-140"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="691c7-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691c7-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="691c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691c7-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="691c7-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="691c7-143">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="691c7-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="691c7-144">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="691c7-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





