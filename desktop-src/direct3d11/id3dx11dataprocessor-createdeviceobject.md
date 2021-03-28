---
title: Метод ID3DX11DataProcessor Креатедевицеобжект (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Создает объект устройства.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Метод Креатедевицеобжект Direct3D 11
- Метод Креатедевицеобжект Direct3D 11, интерфейс ID3DX11DataProcessor
- Интерфейс ID3DX11DataProcessor Direct3D 11, метод Креатедевицеобжект
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356033"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="f27f3-107">Метод ID3DX11DataProcessor:: Креатедевицеобжект</span><span class="sxs-lookup"><span data-stu-id="f27f3-107">ID3DX11DataProcessor::CreateDeviceObject method</span></span>

> [!Note]  
> <span data-ttu-id="f27f3-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f27f3-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f27f3-109">Создает объект устройства.</span><span class="sxs-lookup"><span data-stu-id="f27f3-109">Creates a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f27f3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f27f3-110">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="f27f3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f27f3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f27f3-112">*ппдатаобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f27f3-112">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f27f3-113">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f27f3-113">Type: **void\*\***</span></span>

<span data-ttu-id="f27f3-114">Адрес указателя на созданный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="f27f3-114">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f27f3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f27f3-115">Return value</span></span>

<span data-ttu-id="f27f3-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f27f3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f27f3-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f27f3-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f27f3-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f27f3-118">Remarks</span></span>

<span data-ttu-id="f27f3-119">Этот метод используется [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="f27f3-119">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f27f3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f27f3-120">Requirements</span></span>



| <span data-ttu-id="f27f3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f27f3-121">Requirement</span></span> | <span data-ttu-id="f27f3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f27f3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f27f3-123">Header</span><span class="sxs-lookup"><span data-stu-id="f27f3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f27f3-124"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f27f3-124"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="f27f3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f27f3-125">Library</span></span><br/> | <dl> <span data-ttu-id="f27f3-126"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f27f3-126"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f27f3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f27f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f27f3-128">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="f27f3-128">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="f27f3-129">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f27f3-129">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





