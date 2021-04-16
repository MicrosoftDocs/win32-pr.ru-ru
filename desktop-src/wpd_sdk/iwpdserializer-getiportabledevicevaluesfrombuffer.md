---
description: Метод Жетипортабледевицевалуесфромбуффер десериализует массив байтов в интерфейс Ипортабледевицевалуес.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Метод Ивпдсериализер:: Жетипортабледевицевалуесфромбуффер (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665124"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="ac3e0-103">Метод Ивпдсериализер:: Жетипортабледевицевалуесфромбуффер</span><span class="sxs-lookup"><span data-stu-id="ac3e0-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="ac3e0-104">Метод **жетипортабледевицевалуесфромбуффер** десериализует массив байтов в интерфейс **ипортабледевицевалуес** .</span><span class="sxs-lookup"><span data-stu-id="ac3e0-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac3e0-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="ac3e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac3e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3e0-107">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac3e0-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3e0-108">Указатель на буфер для десериализации.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="ac3e0-109">*двинпутбуфферленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac3e0-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3e0-110">Значение **типа DWORD** , указывающее размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ac3e0-111">*пппарамс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac3e0-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3e0-112">Адрес переменной, которая получает указатель на интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) , созданный из буфера.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="ac3e0-113">Приложение отвечает за вызов **выпуска** в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3e0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac3e0-114">Return value</span></span>

<span data-ttu-id="ac3e0-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac3e0-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac3e0-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ac3e0-117">Return code</span></span>                                                                                  | <span data-ttu-id="ac3e0-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ac3e0-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ac3e0-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ac3e0-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ac3e0-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="ac3e0-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac3e0-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ac3e0-122">Обязательный аргумент-указатель имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="ac3e0-123"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac3e0-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ac3e0-124">Произошла Неуказанная ошибка преобразования.</span><span class="sxs-lookup"><span data-stu-id="ac3e0-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac3e0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ac3e0-125">Requirements</span></span>



| <span data-ttu-id="ac3e0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ac3e0-126">Requirement</span></span> | <span data-ttu-id="ac3e0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ac3e0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3e0-128">Header</span><span class="sxs-lookup"><span data-stu-id="ac3e0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ac3e0-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac3e0-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac3e0-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac3e0-130">Library</span></span><br/> | <dl> <span data-ttu-id="ac3e0-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac3e0-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac3e0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac3e0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3e0-133">**Интерфейс Ивпдсериализер**</span><span class="sxs-lookup"><span data-stu-id="ac3e0-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




