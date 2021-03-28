---
title: Функция D3DX11CreateAsyncMemoryLoader (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создание загрузчика с асинхронной памятью.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- D3DX11CreateAsyncMemoryLoader функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998549"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="bf82d-106">Функция D3DX11CreateAsyncMemoryLoader</span><span class="sxs-lookup"><span data-stu-id="bf82d-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="bf82d-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="bf82d-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="bf82d-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="bf82d-108">See Remarks.</span></span>

 

<span data-ttu-id="bf82d-109">Создание загрузчика с асинхронной памятью.</span><span class="sxs-lookup"><span data-stu-id="bf82d-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf82d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf82d-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="bf82d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf82d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf82d-112">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf82d-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf82d-113">Тип: **[ **лпквоид**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bf82d-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bf82d-114">Указатель на данные.</span><span class="sxs-lookup"><span data-stu-id="bf82d-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="bf82d-115">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf82d-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf82d-116">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bf82d-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bf82d-117">Размер данных.</span><span class="sxs-lookup"><span data-stu-id="bf82d-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="bf82d-118">*ппдаталоадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf82d-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf82d-119">Тип: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bf82d-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="bf82d-120">Адрес указателя на загрузчик асинхронных данных (см. [**интерфейс ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="bf82d-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf82d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf82d-121">Return value</span></span>

<span data-ttu-id="bf82d-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf82d-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf82d-123">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bf82d-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf82d-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf82d-124">Remarks</span></span>

<span data-ttu-id="bf82d-125">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="bf82d-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="bf82d-126">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="bf82d-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="bf82d-127">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="bf82d-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf82d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bf82d-128">Requirements</span></span>



| <span data-ttu-id="bf82d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bf82d-129">Requirement</span></span> | <span data-ttu-id="bf82d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bf82d-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf82d-131">Header</span><span class="sxs-lookup"><span data-stu-id="bf82d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bf82d-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf82d-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="bf82d-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf82d-133">Library</span></span><br/> | <dl> <span data-ttu-id="bf82d-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf82d-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bf82d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf82d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf82d-136">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="bf82d-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

