---
title: Функция D3DX11CreateAsyncResourceLoader (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создайте загрузчик асинхронных ресурсов.
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- D3DX11CreateAsyncResourceLoader функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081908"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="8db2b-106">Функция D3DX11CreateAsyncResourceLoader</span><span class="sxs-lookup"><span data-stu-id="8db2b-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="8db2b-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="8db2b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="8db2b-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="8db2b-108">See Remarks.</span></span>

 

<span data-ttu-id="8db2b-109">Создайте загрузчик асинхронных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8db2b-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db2b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8db2b-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="8db2b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="8db2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db2b-112">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db2b-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db2b-113">Тип: **[ **хмодуле**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8db2b-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8db2b-114">Обработчик для модуля ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8db2b-114">Handle to the resource module.</span></span> <span data-ttu-id="8db2b-115">Для получения маркера используйте [функцию ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="8db2b-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="8db2b-116">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db2b-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db2b-117">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8db2b-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8db2b-118">Имя ресурса в Хсркмодуле.</span><span class="sxs-lookup"><span data-stu-id="8db2b-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="8db2b-119">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="8db2b-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8db2b-120">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8db2b-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="8db2b-121">*ппдаталоадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8db2b-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db2b-122">Тип: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8db2b-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="8db2b-123">Адрес указателя на загрузчик асинхронных данных (см. [**интерфейс ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="8db2b-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db2b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8db2b-124">Return value</span></span>

<span data-ttu-id="8db2b-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8db2b-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8db2b-126">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8db2b-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8db2b-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="8db2b-127">Remarks</span></span>

<span data-ttu-id="8db2b-128">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="8db2b-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="8db2b-129">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="8db2b-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="8db2b-130">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="8db2b-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db2b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="8db2b-131">Requirements</span></span>



| <span data-ttu-id="8db2b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="8db2b-132">Requirement</span></span> | <span data-ttu-id="8db2b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8db2b-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db2b-134">Header</span><span class="sxs-lookup"><span data-stu-id="8db2b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8db2b-135"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db2b-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="8db2b-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8db2b-136">Library</span></span><br/> | <dl> <span data-ttu-id="8db2b-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8db2b-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8db2b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8db2b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db2b-139">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="8db2b-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

