---
description: МКСДК \_ S0PAGE \_ сквозная \_ \_ Структура t представляет собой структуру escape-последовательности мксдк \_ t, \_ \_ объединенную с \_ структурой мксдк S0PAGE \_ Data \_ t.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Структура MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346485"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>МКСДК \_ S0PAGE \_ сквозная \_ Escape- \_ Структура T

**Мксдк \_ S0PAGE \_ сквозная \_ Структура \_ t** представляет собой структуру [**escape-последовательности мксдк \_ \_ \_ t**](mxdcescapeheader.md) , объединенную с структурой [**мксдк \_ S0PAGE \_ Data \_ t**](mxdcs0pagedata.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**мксдцескапе**
</dt> <dd>

Структура [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) с набором элементов **opcode** , равным **мксдкоп \_ Set \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Структура [**MxdcS0PageData**](mxdcs0pagedata.md) , представляющая страницу XPS-документа.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура передается в параметре *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) при вызове с помощью escape-escape-последовательности [**Мксдк \_**](mxdc-escape.md) , а элемент **кода операции** в структуре мксдк в виде заголовка в виде [**\_ \_ \_ T**](mxdcescapeheader.md) — **мксдкоп \_ Set \_ S0PAGE**. В результате конвертер XML-документов Microsoft (МКСДК) передает страницу на принтер, не обрабатывая его.

Выделите память для экранирования, как показано ниже, задайте необходимые поля, а затем вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



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

 

