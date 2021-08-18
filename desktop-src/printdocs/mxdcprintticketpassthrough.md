---
description: '\_ \_ Структура данных мксдк PRINTTICKET \_ содержит билет на печать документа XPS, который содержит параметры принтера и печати, для передачи в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.'
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Структура MXDC_PRINTTICKET_DATA_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 3cf778781340323a78495f87b1408e1011641797ed52a3565bafe41ca450d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471649"
---
# <a name="mxdc_printticket_data_t-structure"></a>\_ \_ Структура T данных мксдк PRINTTICKET \_

Структура **\_ данных мксдк \_ PRINTTICKET \_** содержит билет на печать документа XPS, который содержит параметры принтера и печати, для передачи в выходной файл конвертера документов Microsoft XPS (мксдк) без какой-либо обработки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**двдатасизе**
</dt> <dd>

Размер билета на печать в байтах.

</dd> <dt>

**бдата**
</dt> <dd>

Билет на печать документа XPS.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура добавляется в структуру [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) , для которой в качестве элемента **кода операции** задана **\_ \_ фиксированная \_ страница мксдкоп PrintTicket**, **\_ \_ фиксированный \_ документ PrintTicket мксдкоп** или **\_ \_ фиксированная \_ \_ последовательность документов PrintTicket мксдкоп** , чтобы сделать структуру [**мксдк \_ PrintTicket \_ \_ T**](mxdcprintticketescape.md) . Затем **Структура \_ \_ Escape- \_ последовательности мксдк PRINTTICKET** передается в параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) при вызове с escape-Escape- [**размксдк \_**](mxdc-escape.md) . В результате записывается билет на печать в файл документа XPS.

Если для **кода операции** задана **\_ \_ фиксированная \_ страница мксдкоп PRINTTICKET**, вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Если для **кода операции** задано значение фиксированного **\_ \_ \_ документа мксдкоп PrintTicket** или **мксдкоп \_ PrintTicket \_ \_ \_**, то вызов **екстескапе** должен осуществляться между вызовом [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) и вызовом [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
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

 

