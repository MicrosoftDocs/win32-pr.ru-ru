---
description: Создайте загрузчик асинхронных ресурсов.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: Функция D3DX10CreateAsyncResourceLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0539817ffff75c28af41289fc5197f6440a915bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703715"
---
# <a name="d3dx10createasyncresourceloader-function"></a><span data-ttu-id="27d7e-103">Функция D3DX10CreateAsyncResourceLoader</span><span class="sxs-lookup"><span data-stu-id="27d7e-103">D3DX10CreateAsyncResourceLoader function</span></span>

<span data-ttu-id="27d7e-104">Создайте загрузчик асинхронных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27d7e-104">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27d7e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="27d7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d7e-107">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d7e-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d7e-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27d7e-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27d7e-109">Обработчик для модуля ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27d7e-109">Handle to the resource module.</span></span> <span data-ttu-id="27d7e-110">Для получения маркера используйте [функцию ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="27d7e-110">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="27d7e-111">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27d7e-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d7e-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27d7e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27d7e-113">Имя ресурса в Хсркмодуле.</span><span class="sxs-lookup"><span data-stu-id="27d7e-113">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="27d7e-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="27d7e-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="27d7e-115">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="27d7e-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="27d7e-116">*ппдаталоадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27d7e-116">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27d7e-117">Тип: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="27d7e-117">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="27d7e-118">Адрес указателя на обработчик асинхронных данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="27d7e-118">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d7e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27d7e-119">Return value</span></span>

<span data-ttu-id="27d7e-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27d7e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27d7e-121">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="27d7e-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27d7e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="27d7e-122">Requirements</span></span>



| <span data-ttu-id="27d7e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="27d7e-123">Requirement</span></span> | <span data-ttu-id="27d7e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="27d7e-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d7e-125">Header</span><span class="sxs-lookup"><span data-stu-id="27d7e-125">Header</span></span><br/> | <dl> <span data-ttu-id="27d7e-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d7e-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27d7e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27d7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d7e-128">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="27d7e-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
