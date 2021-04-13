---
title: Интерфейс ID3DX11Effect (D3dx11effect. h)
description: Интерфейс ID3DX11Effect управляет набором объектов состояния, ресурсов и шейдеров для реализации результата отрисовки.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Интерфейс ID3DX11Effect Direct3D 11
- Интерфейс ID3DX11Effect Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395946ea4276bc57595abdeb18e7d1755ca0ff1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998597"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="03ac4-105">Интерфейс ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="03ac4-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="03ac4-106">Интерфейс **ID3DX11Effect** управляет набором объектов состояния, ресурсов и шейдеров для реализации результата отрисовки.</span><span class="sxs-lookup"><span data-stu-id="03ac4-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="03ac4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="03ac4-107">Members</span></span>

<span data-ttu-id="03ac4-108">Интерфейс **ID3DX11Effect** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="03ac4-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="03ac4-109">**ID3DX11Effect** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="03ac4-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="03ac4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="03ac4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="03ac4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="03ac4-111">Methods</span></span>

<span data-ttu-id="03ac4-112">Интерфейс **ID3DX11Effect** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="03ac4-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="03ac4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="03ac4-113">Method</span></span>                                                                     | <span data-ttu-id="03ac4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="03ac4-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03ac4-115">**клониффект**</span><span class="sxs-lookup"><span data-stu-id="03ac4-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="03ac4-116">Создает копию интерфейса Effect.</span><span class="sxs-lookup"><span data-stu-id="03ac4-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="03ac4-117">**жеткласслинкаже**</span><span class="sxs-lookup"><span data-stu-id="03ac4-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="03ac4-118">Возвращает интерфейс компоновки класса.</span><span class="sxs-lookup"><span data-stu-id="03ac4-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="03ac4-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="03ac4-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="03ac4-120">Получение постоянного буфера по индексу.</span><span class="sxs-lookup"><span data-stu-id="03ac4-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="03ac4-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="03ac4-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="03ac4-122">Получение буфера констант по имени.</span><span class="sxs-lookup"><span data-stu-id="03ac4-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="03ac4-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="03ac4-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="03ac4-124">Получение описания воздействия.</span><span class="sxs-lookup"><span data-stu-id="03ac4-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="03ac4-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="03ac4-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="03ac4-126">Получите устройство, которое создало этот результат.</span><span class="sxs-lookup"><span data-stu-id="03ac4-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="03ac4-127">**жетграупбиндекс**</span><span class="sxs-lookup"><span data-stu-id="03ac4-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="03ac4-128">Возвращает группу эффектов по индексу.</span><span class="sxs-lookup"><span data-stu-id="03ac4-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="03ac4-129">**жетграупбинаме**</span><span class="sxs-lookup"><span data-stu-id="03ac4-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="03ac4-130">Возвращает группу эффектов по имени.</span><span class="sxs-lookup"><span data-stu-id="03ac4-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="03ac4-131">**жеттечникуебиндекс**</span><span class="sxs-lookup"><span data-stu-id="03ac4-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="03ac4-132">Получение методики по индексу.</span><span class="sxs-lookup"><span data-stu-id="03ac4-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="03ac4-133">**жеттечникуебинаме**</span><span class="sxs-lookup"><span data-stu-id="03ac4-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="03ac4-134">Получите метод по имени.</span><span class="sxs-lookup"><span data-stu-id="03ac4-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="03ac4-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="03ac4-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="03ac4-136">Возвращает переменную по индексу.</span><span class="sxs-lookup"><span data-stu-id="03ac4-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="03ac4-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="03ac4-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="03ac4-138">Получить переменную по имени.</span><span class="sxs-lookup"><span data-stu-id="03ac4-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="03ac4-139">**жетвариаблебисемантик**</span><span class="sxs-lookup"><span data-stu-id="03ac4-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="03ac4-140">Получить переменную по семантике.</span><span class="sxs-lookup"><span data-stu-id="03ac4-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="03ac4-141">**Оптимизировано**</span><span class="sxs-lookup"><span data-stu-id="03ac4-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="03ac4-142">Протестируйте результат, чтобы проверить, были ли метаданные отражения удалены из памяти.</span><span class="sxs-lookup"><span data-stu-id="03ac4-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="03ac4-143">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="03ac4-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="03ac4-144">Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="03ac4-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="03ac4-145">**Оптимизация**</span><span class="sxs-lookup"><span data-stu-id="03ac4-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="03ac4-146">Сократите объем памяти, необходимый для воздействия.</span><span class="sxs-lookup"><span data-stu-id="03ac4-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="03ac4-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="03ac4-147">Remarks</span></span>

<span data-ttu-id="03ac4-148">Результат создается путем вызова [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="03ac4-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="03ac4-149">Система эффектов группирует сведения, необходимые для подготовки к просмотру, в котором содержатся: объекты состояния для назначения изменений состояния в группах, ресурсы для предоставления входных данных и хранения выходных данных, а также программы, управляющие выполнением отрисовки с помощью шейдеров.</span><span class="sxs-lookup"><span data-stu-id="03ac4-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="03ac4-150">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="03ac4-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="03ac4-151">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="03ac4-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="03ac4-152">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="03ac4-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="03ac4-153">При вызове [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта **ID3DX11Effect** для получения интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) функция **QueryInterface** возвращает E \_ неinterface.</span><span class="sxs-lookup"><span data-stu-id="03ac4-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="03ac4-154">Чтобы обойти эту ошибку, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="03ac4-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="requirements"></a><span data-ttu-id="03ac4-155">Требования</span><span class="sxs-lookup"><span data-stu-id="03ac4-155">Requirements</span></span>
>
> 
>
<span data-ttu-id="03ac4-156">| Требование | Значение |</span><span class="sxs-lookup"><span data-stu-id="03ac4-156">| Requirement | Value |</span></span>
> <span data-ttu-id="03ac4-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Заголовок</span><span class="sxs-lookup"><span data-stu-id="03ac4-157">|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Header</span></span><br/>  | <dl> <span data-ttu-id="03ac4-158"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="03ac4-158"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    <span data-ttu-id="03ac4-159">| | Библиотечная</span><span class="sxs-lookup"><span data-stu-id="03ac4-159">| | Library</span></span><br/> | <dl> <span data-ttu-id="03ac4-160"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="03ac4-160"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |
>
> 
>
> ## <a name="see-also"></a><span data-ttu-id="03ac4-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03ac4-161">See also</span></span>
>
> <dl> <dt>

[<span data-ttu-id="03ac4-162">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="03ac4-162">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="03ac4-163">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="03ac4-163">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>
>
>  
>
>  
>
