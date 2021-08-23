---
description: '\_ \_ Структура escape-последовательности мксдк PRINTTICKET \_ t представляет собой мксдкную структуру \_ \_ заголовка \_ t, объединяющую \_ структуру данных мксдк PrintTicket \_ \_ t.'
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Структура MXDC_PRINTTICKET_ESCAPE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: eca1858bbbf09d4e3c3af8a91f9bb91550eddfd703f59e86112e65c56a43d553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099068"
---
# <a name="mxdc_printticket_escape_t-structure"></a>\_ \_ Структура Escape- \_ T мксдк PRINTTICKET

Структура **\_ Escape- \_ последовательности мксдк PRINTTICKET \_ t** представляет собой [**мксдкную структуру \_ \_ заголовка \_ t**](mxdcescapeheader.md) , объединяющую [**структуру \_ данных мксдк PrintTicket \_ \_ t**](mxdcprintticketpassthrough.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**мксдцескапе**
</dt> <dd>

Структура [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) с набором элементов **opcode** для мксдкоп \_ \_ фиксированной \_ страницы PrintTicket, \_ \_ фиксированный документ PrintTicket мксдкоп или номер \_ \_ \_ фиксированного документа PrintTicket мксдкоп \_ \_ .

</dd> <dt>

**принттиккетдата**
</dt> <dd>

Структура [**\_ данных мксдк \_ PRINTTICKET \_ T**](mxdcprintticketpassthrough.md) , содержащая билет на печать.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура передается в параметре *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , когда эта функция вызывается с помощью escape **\_ \_ \_ -** экранирования [**мксдк \_**](mxdc-escape.md) , а элемент **кода операции** в структуре [**Escape- \_ \_ заголовка \_ мксдк**](mxdcescapeheader.md) — мксдкоп, фиксированный **\_ \_ \_ документ PrintTicket** или **мксдкоп \_ PrintTicket \_ fixed \_ doc \_ Seq**. В результате записывается билет на печать в файл документа XPS.

Выделите память для экранирования, как показано ниже, задайте необходимые поля, а затем вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



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

 

