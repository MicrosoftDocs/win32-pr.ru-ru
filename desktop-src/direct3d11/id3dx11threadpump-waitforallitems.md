---
title: Метод ID3DX11ThreadPump Ваитфораллитемс (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Ожидает завершения всех рабочих элементов в конвейере потока.
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- Метод Ваитфораллитемс Direct3D 11
- Метод Ваитфораллитемс Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Ваитфораллитемс
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40abbab67d6743be2190d5e81c733f63b52b32f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998450"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a><span data-ttu-id="71127-107">Метод ID3DX11ThreadPump:: Ваитфораллитемс</span><span class="sxs-lookup"><span data-stu-id="71127-107">ID3DX11ThreadPump::WaitForAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="71127-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="71127-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="71127-109">Ожидает завершения всех рабочих элементов в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="71127-109">Waits for all work items in the thread pump to finish.</span></span>

## <a name="syntax"></a><span data-ttu-id="71127-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71127-110">Syntax</span></span>


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a><span data-ttu-id="71127-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="71127-111">Parameters</span></span>

<span data-ttu-id="71127-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="71127-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71127-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71127-113">Return value</span></span>

<span data-ttu-id="71127-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71127-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71127-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="71127-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71127-116">Требования</span><span class="sxs-lookup"><span data-stu-id="71127-116">Requirements</span></span>



| <span data-ttu-id="71127-117">Требование</span><span class="sxs-lookup"><span data-stu-id="71127-117">Requirement</span></span> | <span data-ttu-id="71127-118">Значение</span><span class="sxs-lookup"><span data-stu-id="71127-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71127-119">Header</span><span class="sxs-lookup"><span data-stu-id="71127-119">Header</span></span><br/>  | <dl> <span data-ttu-id="71127-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="71127-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="71127-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71127-121">Library</span></span><br/> | <dl> <span data-ttu-id="71127-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71127-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="71127-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71127-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71127-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="71127-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="71127-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="71127-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





