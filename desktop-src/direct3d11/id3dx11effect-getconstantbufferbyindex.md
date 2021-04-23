---
title: Метод ID3DX11Effect Жетконстантбуффербиндекс (D3dx11effect. h)
description: Получение постоянного буфера по индексу.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Метод Жетконстантбуффербиндекс Direct3D 11
- Метод Жетконстантбуффербиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетконстантбуффербиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987098"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="2c4ca-106">Метод ID3DX11Effect:: Жетконстантбуффербиндекс</span><span class="sxs-lookup"><span data-stu-id="2c4ca-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="2c4ca-107">Получение постоянного буфера по индексу.</span><span class="sxs-lookup"><span data-stu-id="2c4ca-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4ca-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c4ca-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="2c4ca-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c4ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4ca-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="2c4ca-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="2c4ca-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2c4ca-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2c4ca-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="2c4ca-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4ca-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c4ca-113">Return value</span></span>

<span data-ttu-id="2c4ca-114">Тип: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c4ca-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="2c4ca-115">Указатель на [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2c4ca-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c4ca-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c4ca-116">Remarks</span></span>

<span data-ttu-id="2c4ca-117">Для действия, содержащего переменную, которая будет доступна для чтения и записи приложением, требуется по крайней мере один буфер константы.</span><span class="sxs-lookup"><span data-stu-id="2c4ca-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="2c4ca-118">Для лучшей производительности результат должен организовывать переменные в один или несколько буферов констант в зависимости от частоты обновления.</span><span class="sxs-lookup"><span data-stu-id="2c4ca-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="2c4ca-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="2c4ca-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2c4ca-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="2c4ca-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2c4ca-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2c4ca-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c4ca-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2c4ca-122">Requirements</span></span>



| <span data-ttu-id="2c4ca-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2c4ca-123">Requirement</span></span> | <span data-ttu-id="2c4ca-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2c4ca-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4ca-125">Header</span><span class="sxs-lookup"><span data-stu-id="2c4ca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2c4ca-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4ca-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2c4ca-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c4ca-127">Library</span></span><br/> | <dl> <span data-ttu-id="2c4ca-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="2c4ca-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c4ca-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c4ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4ca-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="2c4ca-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

