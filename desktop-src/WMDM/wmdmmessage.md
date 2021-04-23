---
title: Перечисление Вмдммессаже
description: Тип перечисления Вмдммессаже определяет типы сообщений и состояния.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Вмдммессаже перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694596"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="085a8-104">Перечисление Вмдммессаже</span><span class="sxs-lookup"><span data-stu-id="085a8-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="085a8-105">Тип перечисления **вмдммессаже** определяет типы сообщений и состояния.</span><span class="sxs-lookup"><span data-stu-id="085a8-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="085a8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="085a8-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="085a8-107">Константы</span><span class="sxs-lookup"><span data-stu-id="085a8-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="085a8-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_ \_ Получение устройства MSG \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="085a8-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="085a8-109">Устройство диспетчер устройств Windows Media подключено.</span><span class="sxs-lookup"><span data-stu-id="085a8-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="085a8-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_ \_ Удаление устройства MSG \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="085a8-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="085a8-111">Удалено устройство диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="085a8-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="085a8-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_ \_ Получение носителя сообщения \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="085a8-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="085a8-113">Носитель вставлен на устройство диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="085a8-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="085a8-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_ \_ Удаление мультимедийного сообщения вмдм \_**</span><span class="sxs-lookup"><span data-stu-id="085a8-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="085a8-115">Носитель был удален с устройства диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="085a8-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="085a8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="085a8-116">Requirements</span></span>



| <span data-ttu-id="085a8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="085a8-117">Requirement</span></span> | <span data-ttu-id="085a8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="085a8-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="085a8-119">Header</span><span class="sxs-lookup"><span data-stu-id="085a8-119">Header</span></span><br/> | <dl> <span data-ttu-id="085a8-120"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="085a8-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="085a8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="085a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085a8-122">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="085a8-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





