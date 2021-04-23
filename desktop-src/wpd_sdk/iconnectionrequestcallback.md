---
description: Определяет один метод обратного вызова.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Интерфейс Иконнектионрекуесткаллбакк (Девпкэй. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999608"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="5d169-103">Интерфейс Иконнектионрекуесткаллбакк</span><span class="sxs-lookup"><span data-stu-id="5d169-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="5d169-104">Интерфейс **иконнектионрекуесткаллбакк** определяет один метод обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="5d169-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="5d169-105">Приложение для переносных устройств Windows (WPD) реализует этот необязательный интерфейс модели COM для получения уведомлений о завершенных запросах и отмене ожидающих запросов.</span><span class="sxs-lookup"><span data-stu-id="5d169-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="5d169-106">Запросы отправляются с помощью методов [**ипортабледевицеконнектор:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) и [**ипортабледевицеконнектор::D соединения**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="5d169-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="5d169-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="5d169-107">Members</span></span>

<span data-ttu-id="5d169-108">Интерфейс **иконнектионрекуесткаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5d169-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d169-109">**Иконнектионрекуесткаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d169-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="5d169-110">Методы</span><span class="sxs-lookup"><span data-stu-id="5d169-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d169-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5d169-111">Methods</span></span>

<span data-ttu-id="5d169-112">Интерфейс **иконнектионрекуесткаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5d169-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="5d169-113">Метод</span><span class="sxs-lookup"><span data-stu-id="5d169-113">Method</span></span>                                                      | <span data-ttu-id="5d169-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5d169-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d169-115">**OnComplete**</span><span class="sxs-lookup"><span data-stu-id="5d169-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="5d169-116">Уведомляет приложение о завершении ранее запланированного запроса.</span><span class="sxs-lookup"><span data-stu-id="5d169-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d169-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5d169-117">Requirements</span></span>



| <span data-ttu-id="5d169-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5d169-118">Requirement</span></span> | <span data-ttu-id="5d169-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5d169-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d169-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d169-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d169-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5d169-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="5d169-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d169-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d169-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5d169-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="5d169-124">Header</span><span class="sxs-lookup"><span data-stu-id="5d169-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d169-125"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d169-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="5d169-126">IDL</span><span class="sxs-lookup"><span data-stu-id="5d169-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d169-127"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d169-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="5d169-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d169-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d169-129"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d169-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

