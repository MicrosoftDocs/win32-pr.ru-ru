---
description: Уведомляет приложение о завершении ранее запланированного запроса подключения или отключения к устройству MTP/Bluetooth.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Метод Иконнектионрекуесткаллбакк:: OnComplete (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911140"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="99f9b-103">Метод Иконнектионрекуесткаллбакк:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="99f9b-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="99f9b-104">Метод **OnComplete** уведомляет приложение о завершении ранее запланированного запроса подключения или отключения к устройству MTP/Bluetooth</span><span class="sxs-lookup"><span data-stu-id="99f9b-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="99f9b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99f9b-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="99f9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99f9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f9b-107">*хрстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99f9b-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99f9b-108">Состояние запроса на подключение или отключение данного устройства.</span><span class="sxs-lookup"><span data-stu-id="99f9b-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f9b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99f9b-109">Return value</span></span>

<span data-ttu-id="99f9b-110">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="99f9b-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="99f9b-111">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="99f9b-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="99f9b-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="99f9b-112">Return code</span></span>                                                                          | <span data-ttu-id="99f9b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="99f9b-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="99f9b-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="99f9b-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="99f9b-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="99f9b-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99f9b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99f9b-116">Remarks</span></span>

<span data-ttu-id="99f9b-117">Приложение реализует интерфейс [**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md) для получения уведомлений о завершенных запросах и отмены ожидающих запросов.</span><span class="sxs-lookup"><span data-stu-id="99f9b-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="99f9b-118">Портативные устройства Windows (WPD) вызывают этот метод, чтобы уведомить приложение о завершении ранее запланированного запроса.</span><span class="sxs-lookup"><span data-stu-id="99f9b-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="99f9b-119">Каждый запрос можно относить и отменять с помощью обратного вызова, предоставленного приложением.</span><span class="sxs-lookup"><span data-stu-id="99f9b-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="99f9b-120">Поэтому, если приложению нужно отправить несколько запросов одновременно с помощью одного и того же объекта [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , каждому запросу должен быть передан уникальный объект [**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md) в качестве входного параметра для методов [**Ипортабледевицеконнектор:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) и [**ипортабледевицеконнектор::D соединения**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="99f9b-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f9b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="99f9b-121">Requirements</span></span>



| <span data-ttu-id="99f9b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="99f9b-122">Requirement</span></span> | <span data-ttu-id="99f9b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="99f9b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f9b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99f9b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99f9b-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="99f9b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="99f9b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99f9b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99f9b-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="99f9b-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="99f9b-128">Header</span><span class="sxs-lookup"><span data-stu-id="99f9b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99f9b-129"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="99f9b-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="99f9b-130">IDL</span><span class="sxs-lookup"><span data-stu-id="99f9b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99f9b-131"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99f9b-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="99f9b-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="99f9b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="99f9b-133"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99f9b-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="99f9b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99f9b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f9b-135">**иконнектионрекуесткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="99f9b-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 




