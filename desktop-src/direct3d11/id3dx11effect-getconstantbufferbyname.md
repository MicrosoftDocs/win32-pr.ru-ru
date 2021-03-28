---
title: Метод ID3DX11Effect Жетконстантбуффербинаме (D3dx11effect. h)
description: Получение буфера констант по имени.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Метод Жетконстантбуффербинаме Direct3D 11
- Метод Жетконстантбуффербинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетконстантбуффербинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914791"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="9e20f-106">Метод ID3DX11Effect:: Жетконстантбуффербинаме</span><span class="sxs-lookup"><span data-stu-id="9e20f-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="9e20f-107">Получение буфера констант по имени.</span><span class="sxs-lookup"><span data-stu-id="9e20f-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e20f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e20f-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="9e20f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e20f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e20f-110">*имя*;</span><span class="sxs-lookup"><span data-stu-id="9e20f-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="9e20f-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e20f-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9e20f-112">Имя константного буфера.</span><span class="sxs-lookup"><span data-stu-id="9e20f-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e20f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e20f-113">Return value</span></span>

<span data-ttu-id="9e20f-114">Тип: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e20f-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="9e20f-115">Указатель на буфер константы, указанный в имени.</span><span class="sxs-lookup"><span data-stu-id="9e20f-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="9e20f-116">См. [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9e20f-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e20f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e20f-117">Remarks</span></span>

<span data-ttu-id="9e20f-118">Для действия, содержащего переменную, которая будет доступна для чтения и записи приложением, требуется по крайней мере один буфер константы.</span><span class="sxs-lookup"><span data-stu-id="9e20f-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="9e20f-119">Для лучшей производительности результат должен организовывать переменные в один или несколько буферов констант в зависимости от частоты обновления.</span><span class="sxs-lookup"><span data-stu-id="9e20f-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="9e20f-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9e20f-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9e20f-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9e20f-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9e20f-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9e20f-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e20f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9e20f-123">Requirements</span></span>



| <span data-ttu-id="9e20f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9e20f-124">Requirement</span></span> | <span data-ttu-id="9e20f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9e20f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e20f-126">Header</span><span class="sxs-lookup"><span data-stu-id="9e20f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9e20f-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e20f-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9e20f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e20f-128">Library</span></span><br/> | <dl> <span data-ttu-id="9e20f-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9e20f-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e20f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e20f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e20f-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="9e20f-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

