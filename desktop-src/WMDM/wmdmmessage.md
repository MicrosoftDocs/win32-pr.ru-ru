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
# <a name="wmdmmessage-enumeration"></a>Перечисление Вмдммессаже

Тип перечисления **вмдммессаже** определяет типы сообщений и состояния.

## <a name="syntax"></a>Синтаксис


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_ \_ Получение устройства MSG \_ вмдм**
</dt> <dd>

Устройство диспетчер устройств Windows Media подключено.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_ \_ Удаление устройства MSG \_ вмдм**
</dt> <dd>

Удалено устройство диспетчер устройств Windows Media.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_ \_ Получение носителя сообщения \_ вмдм**
</dt> <dd>

Носитель вставлен на устройство диспетчер устройств Windows Media.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_ \_ Удаление мультимедийного сообщения вмдм \_**
</dt> <dd>

Носитель был удален с устройства диспетчер устройств Windows Media.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





