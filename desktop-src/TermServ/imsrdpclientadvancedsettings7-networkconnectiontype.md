---
title: IMsRdpClientAdvancedSettings7 Нетворкконнектионтипе, свойство
description: Возвращает или задает тип сетевого подключения, используемого между клиентом и сервером. Сведения о типе сетевого подключения, передаваемые серверу, помогают серверу настроить несколько параметров на основе типа сетевого подключения.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Нетворкконнектионтипе
- Службы удаленных рабочих столов свойства Нетворкконнектионтипе, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Нетворкконнектионтипе
- Службы удаленных рабочих столов свойства Нетворкконнектионтипе, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Нетворкконнектионтипе
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681937"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="9205e-109">Свойство IMsRdpClientAdvancedSettings7:: Нетворкконнектионтипе</span><span class="sxs-lookup"><span data-stu-id="9205e-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="9205e-110">Возвращает или задает тип сетевого подключения, используемого между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="9205e-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="9205e-111">Сведения о типе сетевого подключения, передаваемые серверу, помогают серверу настроить несколько параметров на основе типа сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="9205e-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="9205e-112">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9205e-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9205e-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9205e-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="9205e-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9205e-114">Property value</span></span>

<span data-ttu-id="9205e-115">Тип сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="9205e-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="9205e-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Подключение к \_ Тип \_ модема** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="9205e-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9205e-117">Модем (56 кбит/с)</span><span class="sxs-lookup"><span data-stu-id="9205e-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="9205e-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Подключение к \_ Тип \_ широкополосные \_ низкая** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="9205e-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="9205e-119">Медленное широкополосное подключение (от 256 кбит/с до 2 Мбит/с)</span><span class="sxs-lookup"><span data-stu-id="9205e-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="9205e-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Подключение к \_ Тип \_ спутника** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="9205e-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="9205e-121">Вспомогательная лицензия (от 2 до 16 Мбит/с с высокой задержкой)</span><span class="sxs-lookup"><span data-stu-id="9205e-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="9205e-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Подключение к \_ Тип \_ широкополосного \_ высокого** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="9205e-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="9205e-123">Высокоскоростное широкополосное подключение (от 2 до 10 Мбит/с)</span><span class="sxs-lookup"><span data-stu-id="9205e-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="9205e-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Подключение к \_ Тип \_ WAN** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="9205e-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="9205e-125">Глобальная сеть (WAN) (от 10 Мбит/с и выше с высокой задержкой)</span><span class="sxs-lookup"><span data-stu-id="9205e-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="9205e-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Подключение к \_ Введите \_ локальную сеть** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="9205e-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="9205e-127">Локальная сеть (LAN) (10 Мбит/с или выше)</span><span class="sxs-lookup"><span data-stu-id="9205e-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9205e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9205e-128">Requirements</span></span>



| <span data-ttu-id="9205e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9205e-129">Requirement</span></span> | <span data-ttu-id="9205e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9205e-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9205e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9205e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9205e-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9205e-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="9205e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9205e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9205e-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9205e-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="9205e-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9205e-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="9205e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9205e-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9205e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9205e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9205e-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9205e-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9205e-139">IID</span><span class="sxs-lookup"><span data-stu-id="9205e-139">IID</span></span><br/>                      | <span data-ttu-id="9205e-140">IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="9205e-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9205e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9205e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9205e-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9205e-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9205e-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9205e-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





