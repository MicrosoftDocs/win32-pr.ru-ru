---
description: Метод Вритеипортабледевицевалуестобуффер сериализует интерфейс Ипортабледевицевалуес в выделенный вызывающим объектом массив байтов.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Метод Ивпдсериализер:: Вритеипортабледевицевалуестобуффер (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721005"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="80891-103">Метод Ивпдсериализер:: Вритеипортабледевицевалуестобуффер</span><span class="sxs-lookup"><span data-stu-id="80891-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="80891-104">Метод **вритеипортабледевицевалуестобуффер** сериализует интерфейс **ипортабледевицевалуес** в выделенный вызывающим объектом массив байтов.</span><span class="sxs-lookup"><span data-stu-id="80891-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="80891-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80891-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="80891-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80891-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80891-107">*дваутпутбуфферленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80891-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80891-108">**Параметр DWORD** , указывающий размер *pBuffer* в байтах.</span><span class="sxs-lookup"><span data-stu-id="80891-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="80891-109">*пресултс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80891-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80891-110">Указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) для сериализации.</span><span class="sxs-lookup"><span data-stu-id="80891-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="80891-111">*pBuffer* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80891-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80891-112">Указатель на выделенный вызывающим объектом буфер.</span><span class="sxs-lookup"><span data-stu-id="80891-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="80891-113">Чтобы узнать размер требуемого буфера, вызовите **жетсериализедсизе**.</span><span class="sxs-lookup"><span data-stu-id="80891-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="80891-114">*пдвбитесвриттен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80891-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80891-115">Указатель на **DWORD** , указывающий число байтов, фактически записанных в выделенный вызывающим объектом буфер.</span><span class="sxs-lookup"><span data-stu-id="80891-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80891-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80891-116">Return value</span></span>

<span data-ttu-id="80891-117">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="80891-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="80891-118">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="80891-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="80891-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="80891-119">Return code</span></span>                                                                                   | <span data-ttu-id="80891-120">Описание</span><span class="sxs-lookup"><span data-stu-id="80891-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="80891-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="80891-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="80891-122">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="80891-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="80891-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="80891-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="80891-124">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="80891-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="80891-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="80891-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="80891-126">Предоставленный вызывающим объектом буфер недостаточно велик.</span><span class="sxs-lookup"><span data-stu-id="80891-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80891-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80891-127">Remarks</span></span>

<span data-ttu-id="80891-128">Этот метод копирует интерфейс **ипортабледевицевалуес** в существующий буфер.</span><span class="sxs-lookup"><span data-stu-id="80891-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="80891-129">Если необходимо выделить новый буфер, используйте [**жетбуфферфромипортабледевицевалуес**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="80891-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80891-130">Требования</span><span class="sxs-lookup"><span data-stu-id="80891-130">Requirements</span></span>



| <span data-ttu-id="80891-131">Требование</span><span class="sxs-lookup"><span data-stu-id="80891-131">Requirement</span></span> | <span data-ttu-id="80891-132">Значение</span><span class="sxs-lookup"><span data-stu-id="80891-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80891-133">Header</span><span class="sxs-lookup"><span data-stu-id="80891-133">Header</span></span><br/>  | <dl> <span data-ttu-id="80891-134"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="80891-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="80891-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80891-135">Library</span></span><br/> | <dl> <span data-ttu-id="80891-136"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80891-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80891-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80891-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80891-138">**Интерфейс Ивпдсериализер**</span><span class="sxs-lookup"><span data-stu-id="80891-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




