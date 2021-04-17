---
description: Метод Жетбуфферфромипортабледевицевалуес сериализует отправленный интерфейс Ипортабледевицевалуес в выделенный массив байтов. Возвращаемый массив байтов выделяется для вызывающего объекта и должен быть освобожден вызывающим объектом с помощью CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Метод Ивпдсериализер:: Жетбуфферфромипортабледевицевалуес (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717777"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="675d9-104">Метод Ивпдсериализер:: Жетбуфферфромипортабледевицевалуес</span><span class="sxs-lookup"><span data-stu-id="675d9-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="675d9-105">Метод **жетбуфферфромипортабледевицевалуес** сериализует отправленный интерфейс **ипортабледевицевалуес** в выделенный массив байтов.</span><span class="sxs-lookup"><span data-stu-id="675d9-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="675d9-106">Возвращаемый массив байтов выделяется для вызывающего объекта и должен быть освобожден вызывающим объектом с помощью **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="675d9-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="675d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="675d9-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="675d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="675d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="675d9-109">*псаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="675d9-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="675d9-110">Указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) для сериализации.</span><span class="sxs-lookup"><span data-stu-id="675d9-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="675d9-111">*ппбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="675d9-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="675d9-112">Указатель на **байт \* *_, содержащий сериализованные данные. Портативные устройства Windows распределяют эту память; вызывающий объект должен освободить его, вызвав _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="675d9-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="675d9-113">*пдвбуфферсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="675d9-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="675d9-114">Указатель на **DWORD** , указывающий размер выделенного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="675d9-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="675d9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="675d9-115">Return value</span></span>

<span data-ttu-id="675d9-116">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="675d9-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="675d9-117">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="675d9-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="675d9-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="675d9-118">Return code</span></span>                                                                                   | <span data-ttu-id="675d9-119">Описание</span><span class="sxs-lookup"><span data-stu-id="675d9-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="675d9-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="675d9-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="675d9-121">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="675d9-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="675d9-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="675d9-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="675d9-123">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="675d9-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="675d9-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="675d9-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="675d9-125">Недостаточно памяти для создания буфера.</span><span class="sxs-lookup"><span data-stu-id="675d9-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="675d9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="675d9-126">Requirements</span></span>



| <span data-ttu-id="675d9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="675d9-127">Requirement</span></span> | <span data-ttu-id="675d9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="675d9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675d9-129">Header</span><span class="sxs-lookup"><span data-stu-id="675d9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="675d9-130"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="675d9-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="675d9-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="675d9-131">Library</span></span><br/> | <dl> <span data-ttu-id="675d9-132"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="675d9-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="675d9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="675d9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675d9-134">**Интерфейс Ивпдсериализер**</span><span class="sxs-lookup"><span data-stu-id="675d9-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




