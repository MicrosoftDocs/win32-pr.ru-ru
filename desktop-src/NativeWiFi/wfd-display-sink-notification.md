---
description: Описывает уведомление, передаваемое \_ \_ \_ функции обратного вызова уведомлений для приемника WFD \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Структура WFD_DISPLAY_SINK_NOTIFICATION (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663036"
---
# <a name="wfd_display_sink_notification-structure"></a>\_ \_ Структура уведомлений о приемнике для экрана WFD \_

В **структуре \_ \_ \_ уведомлений о приемнике для представления WFD** описывается уведомление, передаваемое функции [**\_ \_ \_ \_ обратного вызова уведомлений о приемнике для монитора WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Header**
</dt> <dd>

[**\_ \_ \_ \_ Заголовок объекта для приемника WFD**](wfd-display-sink-object-header.md) , описывающий данные, содержащиеся в уведомлении.

</dd> <dt>

**type**
</dt> <dd>

Значение [**\_ \_ \_ \_ типа уведомления о приемнике для представления WFD**](wfd-display-sink-notification-type.md) , которое указывает тип уведомления. Этот параметр также определяет, какие сведения следует использовать в приведенном ниже объединении.

</dd> <dt>

**стрремотедевиценаме**
</dt> <dd>

Содержит строку, завершающуюся НУЛЕМ, которая содержит имя удаленного устройства. \_ \_ Максимальная \_ Длина имени устройства в приемнике WFD \_ \_ определяется как значение (32).

</dd> <dt>

**ремотедевицеаддресс**
</dt> <dd>

[**\_ Mac- \_ адрес DOT11**](dot11-mac-address-type.md) , содержащий BSSID удаленного устройства.

</dd> <dt>

**провисионингрекуестинфо**
</dt> <dd>

Сведения о запросе на подготовку. Используйте этот параметр, если *тип* имеет значение **провисионингрекуестнотификатион**.

<dl> <dt>

**хсессионхандле**
</dt> <dd>

Обработчик сеанса.

</dd> <dt>

**поссиблеконфигмесодс**
</dt> <dd>

Возможные методы для отображения пользовательского интерфейса для интерактивного принятия.

</dd> </dl> </dd> <dt>

**реконнектрекуестинфо**
</dt> <dd>

Сведения о запросе на повторное подключение. Используйте этот параметр, если *тип* имеет значение **реконнектрекуестнотификатион**.

<dl> <dt>

**GroupID**
</dt> <dd>

Идентификатор группы.

</dd> </dl> </dd> <dt>

**коннектединфо**
</dt> <dd>

Сведения о подключенном уведомлении. Используйте этот параметр, если *тип* имеет значение **коннектеднотификатион**.

<dl> <dt>

**хсессионхандле**
</dt> <dd>

Обработчик сеанса.

</dd> <dt>

**гуидсессионинтерфаце**
</dt> <dd>

Идентификатор GUID, указывающий интерфейс сеанса.

</dd> <dt>

**GroupID**
</dt> <dd>

Идентификатор группы.

</dd> <dt>

**стрпрофиле**
</dt> <dd>

Указатель на строку, завершающуюся нулем, описывающую профиль.

</dd> <dt>

**LocalAddress**
</dt> <dd>

Локальный адрес.

</dd> <dt>

**RemoteAddress**
</dt> <dd>

Удаленный адрес.

</dd> <dt>

**уртсппорт**
</dt> <dd>

Порт RTSP.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl> |



 

 




