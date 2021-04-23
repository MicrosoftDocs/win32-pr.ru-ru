---
description: Создание загрузчика асинхронных файлов.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: Функция D3DX10CreateAsyncFileLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713585"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="5fb15-103">Функция D3DX10CreateAsyncFileLoader</span><span class="sxs-lookup"><span data-stu-id="5fb15-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="5fb15-104">Создание загрузчика асинхронных файлов.</span><span class="sxs-lookup"><span data-stu-id="5fb15-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb15-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fb15-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="5fb15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fb15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb15-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5fb15-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb15-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fb15-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5fb15-109">Имя загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="5fb15-109">The name of the file to load.</span></span> <span data-ttu-id="5fb15-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="5fb15-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5fb15-111">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5fb15-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5fb15-112">*ппдаталоадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5fb15-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb15-113">Тип: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5fb15-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="5fb15-114">Адрес указателя на загрузчик асинхронных данных (см. [**интерфейс ID3DX10DataLoader**](id3dx10dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="5fb15-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb15-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fb15-115">Return value</span></span>

<span data-ttu-id="5fb15-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fb15-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fb15-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5fb15-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb15-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5fb15-118">Requirements</span></span>



| <span data-ttu-id="5fb15-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5fb15-119">Requirement</span></span> | <span data-ttu-id="5fb15-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5fb15-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb15-121">Header</span><span class="sxs-lookup"><span data-stu-id="5fb15-121">Header</span></span><br/> | <dl> <span data-ttu-id="5fb15-122"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fb15-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb15-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fb15-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb15-124">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="5fb15-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
