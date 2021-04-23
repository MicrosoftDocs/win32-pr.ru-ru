---
description: Создание конвейера потока.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Функция D3DX10CreateThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000483"
---
# <a name="d3dx10createthreadpump-function"></a><span data-ttu-id="0b047-103">Функция D3DX10CreateThreadPump</span><span class="sxs-lookup"><span data-stu-id="0b047-103">D3DX10CreateThreadPump function</span></span>

<span data-ttu-id="0b047-104">Создание конвейера потока.</span><span class="sxs-lookup"><span data-stu-id="0b047-104">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b047-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b047-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="0b047-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b047-107">*Циосреадс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b047-107">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b047-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b047-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b047-109">Число потоков ввода-вывода для создания.</span><span class="sxs-lookup"><span data-stu-id="0b047-109">The number of I/O threads to create.</span></span> <span data-ttu-id="0b047-110">Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="0b047-110">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0b047-111">*кпроксреадс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b047-111">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b047-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b047-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b047-113">Число создаваемых потоков процесса.</span><span class="sxs-lookup"><span data-stu-id="0b047-113">The number of process threads to create.</span></span> <span data-ttu-id="0b047-114">Если указано значение 0, то Direct3D попытается вычислить оптимальное количество потоков на основе конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="0b047-114">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0b047-115">*ппсреадпумп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b047-115">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b047-116">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0b047-116">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***</span></span>

<span data-ttu-id="0b047-117">Созданный конвейер потока.</span><span class="sxs-lookup"><span data-stu-id="0b047-117">The created thread pump.</span></span> <span data-ttu-id="0b047-118">См. раздел [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0b047-118">See [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b047-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b047-119">Return value</span></span>

<span data-ttu-id="0b047-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b047-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b047-121">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0b047-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b047-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b047-122">Remarks</span></span>

<span data-ttu-id="0b047-123">Конвейер потоков — это очень ресурсоемкий объект.</span><span class="sxs-lookup"><span data-stu-id="0b047-123">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="0b047-124">Для каждого приложения должен быть создан только один конвейер потока.</span><span class="sxs-lookup"><span data-stu-id="0b047-124">Only one thread pump should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b047-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0b047-125">Requirements</span></span>



| <span data-ttu-id="0b047-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0b047-126">Requirement</span></span> | <span data-ttu-id="0b047-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0b047-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b047-128">Header</span><span class="sxs-lookup"><span data-stu-id="0b047-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0b047-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b047-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b047-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0b047-130">Library</span></span><br/> | <dl> <span data-ttu-id="0b047-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b047-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b047-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b047-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b047-133">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="0b047-133">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
