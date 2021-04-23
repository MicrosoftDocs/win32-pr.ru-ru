---
description: Извлекает сведения о загруженном в данный момент наборе модулей для системы.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Функция Ауксклибкуеримодулеинформатион (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656988"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="6cd0a-103">Функция Ауксклибкуеримодулеинформатион</span><span class="sxs-lookup"><span data-stu-id="6cd0a-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="6cd0a-104">Извлекает сведения о загруженном в данный момент наборе модулей для системы.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd0a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cd0a-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6cd0a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cd0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd0a-107">*BufferSize* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6cd0a-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0a-108">На входе — размер буфера *куеринфо* в байтах.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="6cd0a-109">На выходе получает фактический требуемый размер.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-109">On output, receives the actual required size.</span></span> <span data-ttu-id="6cd0a-110">Так как список системных модулей может изменяться между вызовами, это значение также может изменяться между вызовами.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="6cd0a-111">*ElementSize* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cd0a-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0a-112">Размер элемента массива в байтах.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="6cd0a-113">Этот размер определяет формат выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="6cd0a-114">*Куеринфо* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="6cd0a-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0a-115">Указатель на буфер, который получает сведения о модуле.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="6cd0a-116">Эти сведения возвращаются в массиве, элементы которого являются одной из следующих структур: дополнительная информация о вспомогательном [**\_ модуле \_ \_**](aux-module-basic-info-struct.md) или [**\_ \_ Расширенные \_ сведения о модуле AUX**](aux-module-extended-info-struct.md).</span><span class="sxs-lookup"><span data-stu-id="6cd0a-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="6cd0a-117">Конкретная используемая структура зависит от указанного размера элемента.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="6cd0a-118">Если этот параметр имеет **значение NULL**, функция возвращает требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd0a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cd0a-119">Return value</span></span>

<span data-ttu-id="6cd0a-120">Если функция завершается успешно, возвращается значение STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="6cd0a-121">Если функция завершается ошибкой, возвращаемое значение может быть одним из кодов состояния, определенных в файле Ntstatus. h, который доступен в WDK.</span><span class="sxs-lookup"><span data-stu-id="6cd0a-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cd0a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cd0a-122">Remarks</span></span>

<span data-ttu-id="6cd0a-123">Перед вызовом этой функции необходимо вызвать функцию [**ауксклибинитиализе**](auxklibinitialize-func.md) .</span><span class="sxs-lookup"><span data-stu-id="6cd0a-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="6cd0a-124">Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="6cd0a-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd0a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6cd0a-125">Requirements</span></span>



| <span data-ttu-id="6cd0a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6cd0a-126">Requirement</span></span> | <span data-ttu-id="6cd0a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd0a-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd0a-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6cd0a-128">Redistributable</span></span><br/> | <span data-ttu-id="6cd0a-129">Библиотека вспомогательных API Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6cd0a-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="6cd0a-130">Header</span><span class="sxs-lookup"><span data-stu-id="6cd0a-130">Header</span></span><br/>          | <dl> <span data-ttu-id="6cd0a-131"><dt>AUX \_ клиб. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0a-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cd0a-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6cd0a-132">Library</span></span><br/>         | <dl> <span data-ttu-id="6cd0a-133"><dt>AUX \_ клиб. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0a-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd0a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cd0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd0a-135">**ауксклибинитиализе**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="6cd0a-136">**\_ \_ основные \_ сведения о модуле AUX**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="6cd0a-137">**\_ \_ Расширенная \_ информация о модуле AUX**</span><span class="sxs-lookup"><span data-stu-id="6cd0a-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




