---
description: Установка непрерывного диапазона констант шейдера с копированием в памяти.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'Метод ID3DXEffect:: Сетраввалуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703699"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="dfa45-103">Метод ID3DXEffect:: Сетраввалуе</span><span class="sxs-lookup"><span data-stu-id="dfa45-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="dfa45-104">Установка непрерывного диапазона констант шейдера с копированием в памяти.</span><span class="sxs-lookup"><span data-stu-id="dfa45-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfa45-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="dfa45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfa45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa45-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa45-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa45-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="dfa45-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="dfa45-109">Обрабатываемое значение или имя значения, переданного в виде строки.</span><span class="sxs-lookup"><span data-stu-id="dfa45-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="dfa45-110">Передача маркера более эффективна.</span><span class="sxs-lookup"><span data-stu-id="dfa45-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="dfa45-111">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="dfa45-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa45-112">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa45-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa45-113">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="dfa45-113">Type: **void\***</span></span>

<span data-ttu-id="dfa45-114">Указатель на буфер, содержащий данные, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="dfa45-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="dfa45-115">Сетраввалуе проверяет допустимость памяти, но не выполняет проверку допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="dfa45-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="dfa45-116">*Оффсетинбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa45-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa45-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfa45-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfa45-118">Число байтов между началом данных действия и началом константы результата, которые вы собираетесь задать.</span><span class="sxs-lookup"><span data-stu-id="dfa45-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="dfa45-119">*Байт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa45-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa45-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfa45-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfa45-121">Размер устанавливаемого буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="dfa45-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa45-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfa45-122">Return value</span></span>

<span data-ttu-id="dfa45-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dfa45-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dfa45-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="dfa45-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dfa45-125">В случае сбоя метода возвращаемое значение может быть одним из следующих: E \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="dfa45-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa45-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfa45-126">Remarks</span></span>

<span data-ttu-id="dfa45-127">Сетраввалуе — это очень быстрый способ установки констант эффектов, так как он выполняет копирование в памяти без выполнения проверки или преобразования данных (например, преобразование матрицы строкового типа в основную матрицу столбца).</span><span class="sxs-lookup"><span data-stu-id="dfa45-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="dfa45-128">Используйте Сетраввалуе, чтобы задать ряд смежных констант эффектов.</span><span class="sxs-lookup"><span data-stu-id="dfa45-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="dfa45-129">Например, можно задать массив из двадцати матриц с 20 вызовами в [**ID3DXBaseEffect:: сетматрикс**](id3dxbaseeffect--setmatrix.md) или с помощью одного сетраввалуе.</span><span class="sxs-lookup"><span data-stu-id="dfa45-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="dfa45-130">Все значения должны быть либо matrix4x4s, либо float4s, а все матрицы должны быть в основном порядке столбцов.</span><span class="sxs-lookup"><span data-stu-id="dfa45-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="dfa45-131">Значения int или float приводятся к типу float4; Поэтому настоятельно рекомендуется использовать Сетраввалуе только с данными float4 или matrix4x4.</span><span class="sxs-lookup"><span data-stu-id="dfa45-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa45-132">Требования</span><span class="sxs-lookup"><span data-stu-id="dfa45-132">Requirements</span></span>



| <span data-ttu-id="dfa45-133">Требование</span><span class="sxs-lookup"><span data-stu-id="dfa45-133">Requirement</span></span> | <span data-ttu-id="dfa45-134">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa45-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa45-135">Header</span><span class="sxs-lookup"><span data-stu-id="dfa45-135">Header</span></span><br/>  | <dl> <span data-ttu-id="dfa45-136"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa45-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="dfa45-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dfa45-137">Library</span></span><br/> | <dl> <span data-ttu-id="dfa45-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfa45-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dfa45-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfa45-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa45-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="dfa45-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
