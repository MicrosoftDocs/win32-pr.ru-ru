---
title: Метод Optimize ID3DX11Effect (D3dx11effect. h)
description: Сократите объем памяти, необходимый для воздействия.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Метод Optimize, Direct3D 11
- Оптимизация метода Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998603"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="bb8e4-106">Метод ID3DX11Effect:: OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="bb8e4-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="bb8e4-107">Сократите объем памяти, необходимый для воздействия.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb8e4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb8e4-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="bb8e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb8e4-109">Parameters</span></span>

<span data-ttu-id="bb8e4-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb8e4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb8e4-111">Return value</span></span>

<span data-ttu-id="bb8e4-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb8e4-113">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bb8e4-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bb8e4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb8e4-114">Remarks</span></span>

<span data-ttu-id="bb8e4-115">В результате используется два разных способа использования пространства памяти: для хранения сведений, необходимых среде выполнения для выполнения действия, и для хранения метаданных, необходимых для отражения информации обратно в приложение с помощью API.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="bb8e4-116">Можно сократить объем памяти, необходимый для действия, вызвав **ID3DX11Effect:: optimize** , который удаляет метаданные отражения из памяти.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="bb8e4-117">Методы API для считывания переменных больше не будут работать после удаления данных отражения.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="bb8e4-118">Следующие методы будут завершаться ошибкой после того, как будет вызвана оптимизация.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="bb8e4-119">**ID3DX11Effect:: Жетконстантбуффербиндекс**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="bb8e4-120">**ID3DX11Effect:: Жетконстантбуффербинаме**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="bb8e4-121">**ID3DX11Effect:: DESC**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="bb8e4-122">**ID3DX11Effect:: наустройство**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="bb8e4-123">**ID3DX11Effect:: Жеттечникуебиндекс**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="bb8e4-124">**ID3DX11Effect:: Жеттечникуебинаме**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="bb8e4-125">**ID3DX11Effect:: Жетвариаблебиндекс**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="bb8e4-126">**ID3DX11Effect:: Жетвариаблебинаме**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="bb8e4-127">**ID3DX11Effect:: Жетвариаблебисемантик**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="bb8e4-128">Ссылки, извлеченные с помощью этих методов перед вызовом **ID3DX11Effect:: optimize** , по-прежнему действительны после вызова **ID3DX11Effect:: optimize** .</span><span class="sxs-lookup"><span data-stu-id="bb8e4-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="bb8e4-129">Это позволяет приложению получать все переменные, методы и передавать их, вызывать optimize, а затем использовать этот результат.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb8e4-130">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bb8e4-131">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bb8e4-132">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bb8e4-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb8e4-133">Требования</span><span class="sxs-lookup"><span data-stu-id="bb8e4-133">Requirements</span></span>



| <span data-ttu-id="bb8e4-134">Требование</span><span class="sxs-lookup"><span data-stu-id="bb8e4-134">Requirement</span></span> | <span data-ttu-id="bb8e4-135">Значение</span><span class="sxs-lookup"><span data-stu-id="bb8e4-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8e4-136">Header</span><span class="sxs-lookup"><span data-stu-id="bb8e4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="bb8e4-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e4-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bb8e4-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb8e4-138">Library</span></span><br/> | <dl> <span data-ttu-id="bb8e4-139"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e4-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb8e4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb8e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8e4-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="bb8e4-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





