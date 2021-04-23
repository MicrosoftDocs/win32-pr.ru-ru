---
title: Метод destroy ID3DX11DataLoader (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Уничтожает загрузчик после завершения рабочего элемента.
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Метод destroy Direct3D 11
- Метод destroy Direct3D 11, интерфейс ID3DX11DataLoader
- Интерфейс ID3DX11DataLoader Direct3D 11, метод Destroy
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987248"
---
# <a name="id3dx11dataloaderdestroy-method"></a><span data-ttu-id="23707-107">ID3DX11DataLoader: метод:D естрой</span><span class="sxs-lookup"><span data-stu-id="23707-107">ID3DX11DataLoader::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="23707-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="23707-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="23707-109">Уничтожает загрузчик после завершения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="23707-109">Destroys the loader after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="23707-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23707-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="23707-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="23707-111">Parameters</span></span>

<span data-ttu-id="23707-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="23707-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23707-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23707-113">Return value</span></span>

<span data-ttu-id="23707-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23707-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23707-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="23707-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23707-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="23707-116">Remarks</span></span>

<span data-ttu-id="23707-117">Этот метод используется [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="23707-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23707-118">Требования</span><span class="sxs-lookup"><span data-stu-id="23707-118">Requirements</span></span>



| <span data-ttu-id="23707-119">Требование</span><span class="sxs-lookup"><span data-stu-id="23707-119">Requirement</span></span> | <span data-ttu-id="23707-120">Значение</span><span class="sxs-lookup"><span data-stu-id="23707-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23707-121">Header</span><span class="sxs-lookup"><span data-stu-id="23707-121">Header</span></span><br/>  | <dl> <span data-ttu-id="23707-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="23707-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="23707-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23707-123">Library</span></span><br/> | <dl> <span data-ttu-id="23707-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23707-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23707-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23707-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23707-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="23707-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="23707-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="23707-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





