---
title: Метод обработки ID3DX11DataProcessor (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Обрабатывает данные.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Метод обработки Direct3D 11
- Метод Process Direct3D 11, интерфейс ID3DX11DataProcessor
- Интерфейс ID3DX11DataProcessor Direct3D 11, метод Process
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547959"
---
# <a name="id3dx11dataprocessorprocess-method"></a><span data-ttu-id="e2153-107">ID3DX11DataProcessor: метод:P шаблоны</span><span class="sxs-lookup"><span data-stu-id="e2153-107">ID3DX11DataProcessor::Process method</span></span>

> [!Note]  
> <span data-ttu-id="e2153-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="e2153-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="e2153-109">Обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="e2153-109">Processes data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2153-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2153-110">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="e2153-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2153-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2153-112">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2153-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2153-113">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="e2153-113">Type: **void\***</span></span>

<span data-ttu-id="e2153-114">Указатель на данные для обработки.</span><span class="sxs-lookup"><span data-stu-id="e2153-114">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="e2153-115">*кбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2153-115">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2153-116">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2153-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2153-117">Размер данных для обработки.</span><span class="sxs-lookup"><span data-stu-id="e2153-117">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2153-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2153-118">Return value</span></span>

<span data-ttu-id="e2153-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2153-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2153-120">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e2153-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2153-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2153-121">Remarks</span></span>

<span data-ttu-id="e2153-122">Этот метод используется [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="e2153-122">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2153-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e2153-123">Requirements</span></span>



| <span data-ttu-id="e2153-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e2153-124">Requirement</span></span> | <span data-ttu-id="e2153-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e2153-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2153-126">Header</span><span class="sxs-lookup"><span data-stu-id="e2153-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2153-127"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2153-127"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="e2153-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e2153-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2153-129"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2153-129"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2153-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2153-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2153-131">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="e2153-131">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="e2153-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="e2153-132">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

