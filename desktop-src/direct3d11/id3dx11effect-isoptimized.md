---
title: Метод оптимизации ID3DX11Effect (D3dx11effect. h)
description: Протестируйте результат, чтобы проверить, были ли метаданные отражения удалены из памяти.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Метод оптимизации Direct3D 11
- Оптимизированный метод Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, оптимизированный метод
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355540"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="71cb3-106">Метод ID3DX11Effect:: OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="71cb3-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="71cb3-107">Протестируйте результат, чтобы проверить, были ли метаданные отражения удалены из памяти.</span><span class="sxs-lookup"><span data-stu-id="71cb3-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="71cb3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71cb3-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="71cb3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="71cb3-109">Parameters</span></span>

<span data-ttu-id="71cb3-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="71cb3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71cb3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71cb3-111">Return value</span></span>

<span data-ttu-id="71cb3-112">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="71cb3-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="71cb3-113">**Значение true** , если результат оптимизирован. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="71cb3-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="71cb3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="71cb3-114">Remarks</span></span>

<span data-ttu-id="71cb3-115">В результате используется два разных способа использования пространства памяти: для хранения сведений, необходимых среде выполнения для выполнения действия, и для хранения метаданных, необходимых для отражения информации обратно в приложение с помощью API.</span><span class="sxs-lookup"><span data-stu-id="71cb3-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="71cb3-116">Можно сократить объем памяти, необходимый для действия, вызвав [**ID3DX11Effect:: optimize**](id3dx11effect-optimize.md) , который удаляет метаданные отражения из памяти.</span><span class="sxs-lookup"><span data-stu-id="71cb3-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="71cb3-117">Разумеется, методы API для считывания переменных больше не будут работать после удаления данных отражения.</span><span class="sxs-lookup"><span data-stu-id="71cb3-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="71cb3-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="71cb3-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="71cb3-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="71cb3-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="71cb3-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="71cb3-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71cb3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="71cb3-121">Requirements</span></span>



| <span data-ttu-id="71cb3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="71cb3-122">Requirement</span></span> | <span data-ttu-id="71cb3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="71cb3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cb3-124">Header</span><span class="sxs-lookup"><span data-stu-id="71cb3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="71cb3-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="71cb3-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="71cb3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71cb3-126">Library</span></span><br/> | <dl> <span data-ttu-id="71cb3-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="71cb3-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71cb3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71cb3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cb3-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="71cb3-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

