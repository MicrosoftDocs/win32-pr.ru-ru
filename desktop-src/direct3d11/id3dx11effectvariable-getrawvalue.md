---
title: Метод ID3DX11EffectVariable Жетраввалуе (D3dx11effect. h)
description: Получение данных.
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Метод Жетраввалуе Direct3D 11
- Метод Жетраввалуе Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетраввалуе
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987146"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a><span data-ttu-id="8ff08-106">Метод ID3DX11EffectVariable:: Жетраввалуе</span><span class="sxs-lookup"><span data-stu-id="8ff08-106">ID3DX11EffectVariable::GetRawValue method</span></span>

<span data-ttu-id="8ff08-107">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="8ff08-107">Get data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff08-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ff08-108">Syntax</span></span>


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="8ff08-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ff08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff08-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="8ff08-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8ff08-111">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="8ff08-111">Type: **void\***</span></span>

<span data-ttu-id="8ff08-112">Указатель на переменную.</span><span class="sxs-lookup"><span data-stu-id="8ff08-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="8ff08-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="8ff08-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="8ff08-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ff08-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ff08-115">Смещение (в байтах) от начала указателя до данных.</span><span class="sxs-lookup"><span data-stu-id="8ff08-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="8ff08-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="8ff08-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="8ff08-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ff08-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ff08-118">Число получаемых байтов.</span><span class="sxs-lookup"><span data-stu-id="8ff08-118">The number of bytes to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff08-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ff08-119">Return value</span></span>

<span data-ttu-id="8ff08-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ff08-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ff08-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8ff08-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff08-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ff08-122">Remarks</span></span>

<span data-ttu-id="8ff08-123">Этот метод не выполняет преобразование или проверку типа; Таким образом, очень быстрый способ доступа к элементам массива.</span><span class="sxs-lookup"><span data-stu-id="8ff08-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="8ff08-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="8ff08-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8ff08-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="8ff08-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8ff08-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8ff08-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ff08-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8ff08-127">Requirements</span></span>



| <span data-ttu-id="8ff08-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8ff08-128">Requirement</span></span> | <span data-ttu-id="8ff08-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8ff08-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff08-130">Header</span><span class="sxs-lookup"><span data-stu-id="8ff08-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8ff08-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff08-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8ff08-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ff08-132">Library</span></span><br/> | <dl> <span data-ttu-id="8ff08-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="8ff08-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff08-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ff08-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff08-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="8ff08-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

