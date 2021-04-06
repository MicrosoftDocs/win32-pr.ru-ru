---
description: '\_ \_ Структура данных мксдк S0PAGE \_ содержит страницу документа XPS, которая передается в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.'
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Структура MXDC_S0PAGE_DATA_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815345"
---
# <a name="mxdc_s0page_data_t-structure"></a>\_ \_ Структура T мксдк данных S0PAGE \_

Структура **\_ данных мксдк \_ S0PAGE \_** содержит страницу документа XPS, которая передается в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**двсизе**
</dt> <dd>

Размер выходного буфера **бдата**.

</dd> <dt>

**бдата**
</dt> <dd>

Страница документа XPS.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура добавляется в структуру [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) (для которой в качестве **кода операции** задано значение Мксдкоп \_ Set \_ S0PAGE), чтобы сделать [**мксдк \_ S0PAGE \_ сквозной \_ Escape \_**](mxdcs0pagepassthroughescape.md) -структурой t. Эта структура затем передается в параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) при вызове с помощью escape- [**\_ последовательности мксдк**](mxdc-escape.md) в качестве экранирования. В результате МКСДК передает страницу в выходные данные без ее обработки.

Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Вызывающее приложение отвечает за проверку XML страницы документа XPS.

Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **мксдкоп \_ Set \_ S0PAGE \_ Resource** как **код операции** для каждого ресурса на странице, прежде чем вызывать его с **мксдкоп \_ Set \_ S0PAGE**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мксдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**Escape-МКСДК \_**](mxdc-escape.md)
</dt> </dl>

 

