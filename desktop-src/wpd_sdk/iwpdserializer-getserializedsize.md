---
description: Метод Жетсериализедсизе вычисляет размер буфера, необходимого для хранения сериализованного интерфейса Ипортабледевицевалуес.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Метод Ивпдсериализер:: Жетсериализедсизе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665125"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="25ff7-103">Метод Ивпдсериализер:: Жетсериализедсизе</span><span class="sxs-lookup"><span data-stu-id="25ff7-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="25ff7-104">Метод **жетсериализедсизе** вычисляет размер буфера, необходимого для хранения сериализованного интерфейса [**ипортабледевицевалуес**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="25ff7-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ff7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25ff7-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="25ff7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25ff7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ff7-107">*псаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25ff7-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff7-108">Указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) , размер которого необходимо запросить.</span><span class="sxs-lookup"><span data-stu-id="25ff7-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="25ff7-109">*пдвсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="25ff7-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25ff7-110">Указатель на **DWORD** , указывающий размер буфера, необходимый для сериализации *псаурце*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="25ff7-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ff7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25ff7-111">Return value</span></span>

<span data-ttu-id="25ff7-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="25ff7-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="25ff7-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="25ff7-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="25ff7-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="25ff7-114">Return code</span></span>                                                                                   | <span data-ttu-id="25ff7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="25ff7-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25ff7-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="25ff7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="25ff7-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="25ff7-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="25ff7-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="25ff7-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="25ff7-119">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="25ff7-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="25ff7-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25ff7-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="25ff7-121">Недостаточно свободной памяти для создания буфера.</span><span class="sxs-lookup"><span data-stu-id="25ff7-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25ff7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="25ff7-122">Requirements</span></span>



| <span data-ttu-id="25ff7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="25ff7-123">Requirement</span></span> | <span data-ttu-id="25ff7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="25ff7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25ff7-125">Header</span><span class="sxs-lookup"><span data-stu-id="25ff7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="25ff7-126"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ff7-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="25ff7-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25ff7-127">Library</span></span><br/> | <dl> <span data-ttu-id="25ff7-128"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25ff7-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ff7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25ff7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ff7-130">**Интерфейс Ивпдсериализер**</span><span class="sxs-lookup"><span data-stu-id="25ff7-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




