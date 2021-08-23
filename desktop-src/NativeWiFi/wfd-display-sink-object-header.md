---
description: Описывает данные объекта отображаемого приемника, входящие в уведомление или результат уведомления.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Структура WFD_DISPLAY_SINK_OBJECT_HEADER (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: e4c9e4d83fbac1cccb2dbc0643acc707176be433dfca7854395a0f97c9c36435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800474"
---
# <a name="wfd_display_sink_object_header-structure"></a>\_ \_ \_ Структура заголовка объекта приемника WFD \_

Структура **\_ \_ \_ \_ заголовка объекта для приемника WFD** описывает данные объекта приемника, входящие в уведомление или результат уведомления.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**Тип**
</dt> <dd>

Тип объекта приемника дисплея. Можно использовать идентификатор **\_ \_ типа объекта приемника WFD \_ \_ \_ по умолчанию** , который определен как значение 1.

</dd> <dt>

**Редакции**
</dt> <dd>

Версия редакции объекта приемника экрана. Можно использовать идентификатор WFD, **\_ \_ \_ \_ редакция \_ \_ 1 объекта приемника** , который определен как значение 1.

</dd> <dt>

**Длина**
</dt> <dd>

Длина данных в уведомлении или в результатах уведомления.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl> |



 

 




