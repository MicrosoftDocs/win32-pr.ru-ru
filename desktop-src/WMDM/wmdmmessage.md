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
ms.openlocfilehash: 348092e079428e0b147d8143411cee7766365913115f968ed0e112b209383077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862664"
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

устройство диспетчер устройств Windows мультимедиа было подключено к сети.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_ \_ Удаление устройства MSG \_ вмдм**
</dt> <dd>

устройство диспетчер устройств Windows носителя было удалено.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_ \_ Получение носителя сообщения \_ вмдм**
</dt> <dd>

носитель вставлен на устройство Windows media диспетчер устройств.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_ \_ Удаление мультимедийного сообщения вмдм \_**
</dt> <dd>

носитель был удален с устройства Windows media диспетчер устройств.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





