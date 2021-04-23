---
title: Метод Load ID3DX11DataLoader (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Загружает данные с диска.
ms.assetid: 21dee078-af8f-4ca1-bb2e-d4ecc0471609
keywords:
- Метод Load, Direct3D 11
- Метод Load Direct3D 11, интерфейс ID3DX11DataLoader
- Интерфейс ID3DX11DataLoader Direct3D 11, метод Load
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Load
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f720a5e6884bfdf1935c6d93f7a05decae5e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987251"
---
# <a name="id3dx11dataloaderload-method"></a><span data-ttu-id="0733b-107">Метод ID3DX11DataLoader:: Load</span><span class="sxs-lookup"><span data-stu-id="0733b-107">ID3DX11DataLoader::Load method</span></span>

> [!Note]  
> <span data-ttu-id="0733b-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="0733b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="0733b-109">Загружает данные с диска.</span><span class="sxs-lookup"><span data-stu-id="0733b-109">Loads data from a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="0733b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0733b-110">Syntax</span></span>


```C++
HRESULT Load();
```



## <a name="parameters"></a><span data-ttu-id="0733b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0733b-111">Parameters</span></span>

<span data-ttu-id="0733b-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0733b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0733b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0733b-113">Return value</span></span>

<span data-ttu-id="0733b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0733b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0733b-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0733b-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0733b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0733b-116">Remarks</span></span>

<span data-ttu-id="0733b-117">Этот метод используется [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0733b-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0733b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0733b-118">Requirements</span></span>



| <span data-ttu-id="0733b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0733b-119">Requirement</span></span> | <span data-ttu-id="0733b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0733b-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0733b-121">Header</span><span class="sxs-lookup"><span data-stu-id="0733b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0733b-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0733b-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="0733b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0733b-123">Library</span></span><br/> | <dl> <span data-ttu-id="0733b-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0733b-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0733b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0733b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0733b-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="0733b-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="0733b-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="0733b-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





