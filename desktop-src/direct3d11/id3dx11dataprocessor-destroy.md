---
title: Метод destroy ID3DX11DataProcessor (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Уничтожает процессор после завершения рабочего элемента.
ms.assetid: 759641c0-ef86-42ee-88b9-3fcb7a171d86
keywords:
- Метод destroy Direct3D 11
- Метод destroy Direct3D 11, интерфейс ID3DX11DataProcessor
- Интерфейс ID3DX11DataProcessor Direct3D 11, метод Destroy
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af92f8b3a22ba9a62258e8b24589a662eda22592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914815"
---
# <a name="id3dx11dataprocessordestroy-method"></a><span data-ttu-id="9df1f-107">ID3DX11DataProcessor: метод:D естрой</span><span class="sxs-lookup"><span data-stu-id="9df1f-107">ID3DX11DataProcessor::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="9df1f-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="9df1f-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="9df1f-109">Уничтожает процессор после завершения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="9df1f-109">Destroys the processor after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df1f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9df1f-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="9df1f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9df1f-111">Parameters</span></span>

<span data-ttu-id="9df1f-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9df1f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9df1f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9df1f-113">Return value</span></span>

<span data-ttu-id="9df1f-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9df1f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9df1f-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9df1f-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9df1f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9df1f-116">Remarks</span></span>

<span data-ttu-id="9df1f-117">Этот метод используется [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="9df1f-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9df1f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9df1f-118">Requirements</span></span>



| <span data-ttu-id="9df1f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9df1f-119">Requirement</span></span> | <span data-ttu-id="9df1f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9df1f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9df1f-121">Header</span><span class="sxs-lookup"><span data-stu-id="9df1f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9df1f-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df1f-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="9df1f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9df1f-123">Library</span></span><br/> | <dl> <span data-ttu-id="9df1f-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9df1f-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9df1f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9df1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df1f-126">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="9df1f-126">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="9df1f-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="9df1f-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





