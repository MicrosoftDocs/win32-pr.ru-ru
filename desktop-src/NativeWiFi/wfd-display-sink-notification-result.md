---
description: Описывает результат, который при необходимости можно задать после обработки уведомления приемника \_ \_ \_ уведомлений в \_ функции обратного вызова уведомления приемника WFD.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Структура WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Вфдсинк. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664485"
---
# <a name="wfd_display_sink_notification_result-structure"></a>\_ \_ \_ Структура результата уведомления приемника для дисплея WFD \_

В **структуре \_ \_ \_ \_ результатов уведомлений о приемнике WFD отображаются сведения о** результатах, которые можно задать после обработки уведомления приемника уведомлений в функции [**\_ \_ \_ \_ обратного вызова уведомления приемника WFD**](wfd-display-sink-notification-callback.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Header**
</dt> <dd>

[**\_ \_ \_ \_ Заголовок объекта для приемника WFD**](wfd-display-sink-object-header.md) , описывающий данные, включаемые в результат уведомления.

</dd> <dt>

**type**
</dt> <dd>

Значение [**\_ \_ \_ \_ типа уведомления о приемнике представления WFD**](wfd-display-sink-notification-type.md) , которое указывает тип результата уведомления. Этот параметр также определяет, какие сведения следует использовать в приведенном ниже объединении.

</dd> <dt>

**провисионингдата**
</dt> <dd>

Сведения о результате запроса на подготовку. Используйте этот параметр, если *тип* имеет значение **провисионингрекуестнотификатион**.

<dl> <dt>

**конфигмесод**
</dt> <dd>

Метод отображения пользовательского интерфейса для интерактивного принятия.

</dd> <dt>

**упасскэйленгс**
</dt> <dd>

Число расширенных символов в *ключе доступа*, при котором не учитываются признаки конца строки null.

</dd> <dt>

**Наличия**
</dt> <dd>

Содержит ключ Pass в виде массива расширенных символов. \_ \_ Сведения о WPS приемника WFD \_ \_ Максимальная \_ \_ Длина ключа доступа определяется как значение (8).

</dd> </dl> </dd> <dt>

**реконнектдата**
</dt> <dd>

Сведения о результате запроса на повторное подключение. Используйте этот параметр, если *тип* имеет значение **реконнектрекуестнотификатион**.

<dl> <dt>

**стрпрофиле**
</dt> <dd>

Указатель на строку, завершающуюся нулем, описывающую профиль.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl> |



 

 




