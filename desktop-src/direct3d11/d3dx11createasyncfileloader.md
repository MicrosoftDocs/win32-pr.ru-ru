---
title: Функция D3DX11CreateAsyncFileLoader (D3DX11async. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. См. заметки. Создание загрузчика асинхронных файлов.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- D3DX11CreateAsyncFileLoader функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637b2eddb035d937315582188295d93d9fd0e9b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998558"
---
# <a name="d3dx11createasyncfileloader-function"></a><span data-ttu-id="f2fa8-106">Функция D3DX11CreateAsyncFileLoader</span><span class="sxs-lookup"><span data-stu-id="f2fa8-106">D3DX11CreateAsyncFileLoader function</span></span>

> [!Note]  
> <span data-ttu-id="f2fa8-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="f2fa8-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-108">See Remarks.</span></span>

 

<span data-ttu-id="f2fa8-109">Создание загрузчика асинхронных файлов.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-109">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fa8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2fa8-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="f2fa8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2fa8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fa8-112">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2fa8-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fa8-113">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f2fa8-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f2fa8-114">Имя загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-114">The name of the file to load.</span></span> <span data-ttu-id="f2fa8-115">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f2fa8-116">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="f2fa8-117">*ппдаталоадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f2fa8-117">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fa8-118">Тип: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f2fa8-118">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="f2fa8-119">Адрес указателя на загрузчик асинхронных данных (см. [**интерфейс ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="f2fa8-119">Address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fa8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2fa8-120">Return value</span></span>

<span data-ttu-id="f2fa8-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2fa8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2fa8-122">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f2fa8-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2fa8-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2fa8-123">Remarks</span></span>

<span data-ttu-id="f2fa8-124">Нет реализации асинхронного загрузчика за пределами D3DX 10 и D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-124">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="f2fa8-125">Для приложений Магазина Windows примеры DirectX (например, [Пример учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) включают модуль **басиклоадер** , который использует модель асинхронного программирования среда выполнения Windows ([**метод asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="f2fa8-125">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="f2fa8-126">Для классических приложений Win32 можно использовать [Среда выполнения с параллелизмом](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) для реализации чего-то, что аналогично среда выполнения Windows асинхронной модели программирования.</span><span class="sxs-lookup"><span data-stu-id="f2fa8-126">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fa8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f2fa8-127">Requirements</span></span>



| <span data-ttu-id="f2fa8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f2fa8-128">Requirement</span></span> | <span data-ttu-id="f2fa8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f2fa8-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2fa8-130">Header</span><span class="sxs-lookup"><span data-stu-id="f2fa8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f2fa8-131"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2fa8-131"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="f2fa8-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2fa8-132">Library</span></span><br/> | <dl> <span data-ttu-id="f2fa8-133"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2fa8-133"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f2fa8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2fa8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fa8-135">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="f2fa8-135">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

