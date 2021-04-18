---
title: Константы TS_AS_ (Текстстор. h)
description: Следующие флаги задают события, вызывающие методы AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682037"
---
# <a name="ts_as_-constants"></a>TS \_ в качестве \_ \* констант

Следующие флаги задают события, вызывающие методы **AdviseSink** .



| Константа/значение                                                                                                                                                                                                                                                                                                                                         | Описание                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_ \_ \_ Изменение текста**</dt> <dt>(0x1)</dt> </dl>                                                                                                               | В документе изменяется текст.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_ \_ \_ Изменение SEL**</dt> <dt>(0x2)</dt> </dl>                                                                                                                  | Текст, выделенный в документе.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_ \_ \_ Изменение макета**</dt> <dt>(0x4)</dt> </dl>                                                                                                         | Изменяется макет документа.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ КАК \_ \_ изменение attr**</dt> <dt>(0x8)</dt> </dl>                                                                                                               | Атрибуты документа изменяются.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_ При \_ \_ изменении состояния**</dt> <dt>(0x10)</dt> </dl>                                                                                                        | Изменилось состояние документа.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_ так как \_ все \_ приемники**</dt> <dt>(TS \_ As \_ Text меняют TS как SEL меняют состояние TS как attr изменяют TS при изменении \_ \| \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \| \_ \_ состояния \_ )</dt> </dl> | Одно из предыдущих четырех событий, произошедших в документе.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                         |
| Header<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



 

 





