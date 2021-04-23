---
description: Обработка некоторых данных.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: 'ID3DX10DataProcessor: метод:P шаблоны (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273989"
---
# <a name="id3dx10dataprocessorprocess-method"></a><span data-ttu-id="69b7e-103">ID3DX10DataProcessor: метод:P шаблоны</span><span class="sxs-lookup"><span data-stu-id="69b7e-103">ID3DX10DataProcessor::Process method</span></span>

<span data-ttu-id="69b7e-104">Обработка некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="69b7e-104">Process some data.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69b7e-105">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="69b7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69b7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b7e-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69b7e-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b7e-108">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="69b7e-108">Type: **void\***</span></span>

<span data-ttu-id="69b7e-109">Указатель на данные для обработки.</span><span class="sxs-lookup"><span data-stu-id="69b7e-109">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="69b7e-110">*кбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69b7e-110">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b7e-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69b7e-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69b7e-112">Размер данных для обработки.</span><span class="sxs-lookup"><span data-stu-id="69b7e-112">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b7e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69b7e-113">Return value</span></span>

<span data-ttu-id="69b7e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69b7e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69b7e-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="69b7e-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69b7e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="69b7e-116">Requirements</span></span>



| <span data-ttu-id="69b7e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="69b7e-117">Requirement</span></span> | <span data-ttu-id="69b7e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="69b7e-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69b7e-119">Header</span><span class="sxs-lookup"><span data-stu-id="69b7e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="69b7e-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b7e-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69b7e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69b7e-121">Library</span></span><br/> | <dl> <span data-ttu-id="69b7e-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69b7e-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b7e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69b7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b7e-124">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="69b7e-124">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="69b7e-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="69b7e-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
