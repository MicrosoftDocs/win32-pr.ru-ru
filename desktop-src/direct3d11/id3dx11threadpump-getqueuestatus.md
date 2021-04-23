---
title: Метод ID3DX11ThreadPump Жеткуеуестатус (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Возвращает количество элементов в каждой из трех очередей в конвейере потока.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Метод Жеткуеуестатус Direct3D 11
- Метод Жеткуеуестатус Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Жеткуеуестатус
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986906"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="f5a5a-107">Метод ID3DX11ThreadPump:: Жеткуеуестатус</span><span class="sxs-lookup"><span data-stu-id="f5a5a-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="f5a5a-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f5a5a-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f5a5a-109">Возвращает количество элементов в каждой из трех очередей в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="f5a5a-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a5a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5a5a-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="f5a5a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5a5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a5a-112">*пиокуеуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5a5a-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a5a-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f5a5a-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f5a5a-114">Число элементов в очереди ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f5a5a-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="f5a5a-115">*ппроцесскуеуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5a5a-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a5a-116">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f5a5a-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f5a5a-117">Число элементов в очереди процессов.</span><span class="sxs-lookup"><span data-stu-id="f5a5a-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="f5a5a-118">*пдевицекуеуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5a5a-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a5a-119">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f5a5a-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f5a5a-120">Число элементов в очереди устройства.</span><span class="sxs-lookup"><span data-stu-id="f5a5a-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a5a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5a5a-121">Return value</span></span>

<span data-ttu-id="f5a5a-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f5a5a-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f5a5a-123">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f5a5a-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a5a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f5a5a-124">Requirements</span></span>



| <span data-ttu-id="f5a5a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a5a-125">Requirement</span></span> | <span data-ttu-id="f5a5a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f5a5a-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a5a-127">Header</span><span class="sxs-lookup"><span data-stu-id="f5a5a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f5a5a-128"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a5a-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="f5a5a-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5a5a-129">Library</span></span><br/> | <dl> <span data-ttu-id="f5a5a-130"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a5a-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5a5a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5a5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a5a-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="f5a5a-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="f5a5a-133">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f5a5a-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

