---
title: Функция D3DX11CreateThreadPump (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создание конвейера потока.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- D3DX11CreateThreadPump функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987011"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="7e95f-106">Функция D3DX11CreateThreadPump</span><span class="sxs-lookup"><span data-stu-id="7e95f-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="7e95f-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="7e95f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="7e95f-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="7e95f-108">See Remarks.</span></span>

 

<span data-ttu-id="7e95f-109">Создание конвейера потока.</span><span class="sxs-lookup"><span data-stu-id="7e95f-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e95f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e95f-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="7e95f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e95f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e95f-112">*Циосреадс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e95f-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e95f-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7e95f-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7e95f-114">Число потоков ввода-вывода для создания.</span><span class="sxs-lookup"><span data-stu-id="7e95f-114">The number of I/O threads to create.</span></span> <span data-ttu-id="7e95f-115">Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="7e95f-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7e95f-116">*кпроксреадс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e95f-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e95f-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7e95f-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7e95f-118">Число создаваемых потоков процесса.</span><span class="sxs-lookup"><span data-stu-id="7e95f-118">The number of process threads to create.</span></span> <span data-ttu-id="7e95f-119">Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="7e95f-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7e95f-120">*ппсреадпумп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7e95f-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e95f-121">Тип: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7e95f-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="7e95f-122">Созданный конвейер потока.</span><span class="sxs-lookup"><span data-stu-id="7e95f-122">The created thread pump.</span></span> <span data-ttu-id="7e95f-123">См. раздел [**интерфейс ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="7e95f-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e95f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e95f-124">Return value</span></span>

<span data-ttu-id="7e95f-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e95f-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e95f-126">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7e95f-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e95f-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e95f-127">Remarks</span></span>

<span data-ttu-id="7e95f-128">Конвейер потоков — это очень ресурсоемкий объект.</span><span class="sxs-lookup"><span data-stu-id="7e95f-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="7e95f-129">Для каждого приложения должен быть создан только один конвейер потока.</span><span class="sxs-lookup"><span data-stu-id="7e95f-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="7e95f-130">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="7e95f-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="7e95f-131">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="7e95f-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="7e95f-132">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="7e95f-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e95f-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7e95f-133">Requirements</span></span>



| <span data-ttu-id="7e95f-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7e95f-134">Requirement</span></span> | <span data-ttu-id="7e95f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7e95f-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e95f-136">Header</span><span class="sxs-lookup"><span data-stu-id="7e95f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7e95f-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e95f-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="7e95f-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7e95f-138">Library</span></span><br/> | <dl> <span data-ttu-id="7e95f-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e95f-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e95f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e95f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e95f-141">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="7e95f-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

