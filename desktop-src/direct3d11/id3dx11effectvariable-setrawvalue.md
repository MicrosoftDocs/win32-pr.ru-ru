---
title: Метод ID3DX11EffectVariable Сетраввалуе (D3dx11effect. h)
description: Настройка данных.
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- Метод Сетраввалуе Direct3D 11
- Метод Сетраввалуе Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Сетраввалуе
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5186e55b8b1d3472cb25ea6fa067988d4fb1f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273708"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a><span data-ttu-id="15a6e-106">Метод ID3DX11EffectVariable:: Сетраввалуе</span><span class="sxs-lookup"><span data-stu-id="15a6e-106">ID3DX11EffectVariable::SetRawValue method</span></span>

<span data-ttu-id="15a6e-107">Настройка данных.</span><span class="sxs-lookup"><span data-stu-id="15a6e-107">Set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a6e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15a6e-108">Syntax</span></span>


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="15a6e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="15a6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a6e-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="15a6e-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="15a6e-111">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="15a6e-111">Type: **void\***</span></span>

<span data-ttu-id="15a6e-112">Указатель на переменную.</span><span class="sxs-lookup"><span data-stu-id="15a6e-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="15a6e-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="15a6e-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="15a6e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="15a6e-115">Смещение (в байтах) от начала указателя до данных.</span><span class="sxs-lookup"><span data-stu-id="15a6e-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="15a6e-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="15a6e-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="15a6e-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="15a6e-118">Число байтов, которое необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="15a6e-118">The number of bytes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a6e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15a6e-119">Return value</span></span>

<span data-ttu-id="15a6e-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15a6e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15a6e-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="15a6e-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15a6e-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="15a6e-122">Remarks</span></span>

<span data-ttu-id="15a6e-123">Этот метод не выполняет преобразование или проверку типа; Таким образом, очень быстрый способ доступа к элементам массива.</span><span class="sxs-lookup"><span data-stu-id="15a6e-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="15a6e-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="15a6e-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="15a6e-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="15a6e-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="15a6e-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="15a6e-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15a6e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="15a6e-127">Requirements</span></span>



| <span data-ttu-id="15a6e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="15a6e-128">Requirement</span></span> | <span data-ttu-id="15a6e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="15a6e-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a6e-130">Header</span><span class="sxs-lookup"><span data-stu-id="15a6e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="15a6e-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="15a6e-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15a6e-132">Library</span></span><br/> | <dl> <span data-ttu-id="15a6e-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a6e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15a6e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a6e-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="15a6e-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

