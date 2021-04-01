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
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909427"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Вфдсинк. h</dt> </dl> |



 

 




