---
description: Структура МКСДК \_ Escape- \_ заголовка \_ T содержит код операции для вызова екстескапе с escape-мксдк в \_ качестве параметра нескапе. Он также предоставляет размеры входных и выходных буферов.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Структура MXDC_ESCAPE_HEADER_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913147"
---
# <a name="mxdc_escape_header_t-structure"></a>МКСДК \_ T-структура Escape- \_ заголовка \_

Структура **мксдк \_ Escape \_ -заголовка \_ T** содержит код операции для вызова [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с [**\_ escape-мксдк**](mxdc-escape.md) в качестве параметра *нескапе* . Он также предоставляет размеры входных и выходных буферов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбинпут**
</dt> <dd>

Размер входного буфера, который будет передан в параметр *лпсзаутдата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**кбаутпут**
</dt> <dd>

Размер выходного буфера. Это то же значение, что и параметр *кбаутпут* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**транслируют**
</dt> <dd>

Константа кода, которая сообщает МКСДК, что делать.



| Код операции                      | Описание                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| МКСДКОП \_ получить \_ имя файла                | Возвращает, в параметре *лпсзаутдата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) либо полный путь к выходному файлу в виде строки, завершающейся нулем, либо размер этой строки. См. заметки.                   |
| \_ \_ фиксированная \_ последовательность документов мксдкоп PRINTTICKET \_ | Связывает билет на печать с фиксированной последовательностью документов XPS.                                                                                                                                                         |
| \_ \_ фиксированный документ мксдкоп PRINTTICKET \_      | Связывает билет печати с документом XPS.                                                                                                                                                                        |
| \_ \_ фиксированная страница мксдкоп PRINTTICKET \_     | Связывает билет на печать со страницей XPS.                                                                                                                                                                            |
| МКСДКОП \_ Set \_ S0PAGE                  | Отправляет в выходные данные разметку XPS текущей страницы.                                                                                                                                                                |
| МКСДКОП \_ задать \_ S0PAGE \_ ресурс        | Отправляет на выход на страницу ресурс, например изображение или шрифт.                                                                                                                                                 |
| МКСДКОП \_ Set \_ кспспасссру \_ mode       | Помещает МКСДК в сквозное состояние, позволяя приложению записывать XPS непосредственно в выходной файл без какой-либо обработки МКСДК. Таким образом может быть написан весь документ или даже последовательность документов. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Перед вызовом [**\_ escape-последовательности мксдк**](mxdc-escape.md) \_ приложения должны сначала проверить, является ли драйвер Мксдк, вызвав [**ЕКСТЕСКАПЕ**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с помощью escape- [**технологии**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Если драйвер является МКСДК, функция возвращает строку "", завершающуюся нулем http://schemas.microsoft.com/xps/2005/06 .

Эта структура всегда находится в начале данных, передаваемых функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) в его параметре *лпсзиндата* .

Когда **код операции** -мксдкоп \_ получает \_ имя файла:

-   Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит только из структуры **escape-заголовка мксдк \_ \_ \_ T** .
-   Получите выходное имя файла, вызвав [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) дважды.
    1.  В первый раз передайте 4 параметру *Кбаутпут* [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Задайте параметр *лпсзаутдата* , чтобы он указывал на любой выделенный 4 байта памяти. Размер полного пути к файлу будет возвращен в параметре *лпсзаутдата* объекта **екстескапе**.
    2.  Затем вызовите функцию еще раз. На этот раз оба параметра *кбаутпут* и *кбинпут* заданы как 4 + *DataSize*. Полный путь к файлу будет возвращен в структуре [**мксдкжетфиленамедата**](mxdcgetfilenamedata.md) .

Если **код операции** — мксдкоп \_ PrintTicket \_ фиксированный \_ документ \_ Seq или мксдкоп \_ PrintTicket \_ фиксированный \_ документ:

-   Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**мксдкпринттиккетпасссраугх**](mxdcprintticketpassthrough.md) , Объединенной в структуру [**мксдкпринттиккетескапе**](mxdcprintticketescape.md) .
-   Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) и вызовом [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Если **код операции** — \_ это \_ фиксированная страница мксдкоп PRINTTICKET \_ :

-   Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**мксдкпринттиккетпасссраугх**](mxdcprintticketpassthrough.md) , Объединенной в структуру [**мксдкпринттиккетескапе**](mxdcprintticketescape.md) .
-   Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Когда **код операции** — мксдкоп \_ Set \_ S0PAGE:

-   Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**MxdcS0PageData**](mxdcs0pagedata.md) , Объединенной в структуру [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .
-   Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   Вызывающее приложение отвечает за проверку XML.
-   Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с мксдкоп \_ Set \_ S0PAGE \_ Resource как **код операции** для каждого ресурса на странице, прежде чем вызывать его с мксдкоп \_ Set \_ S0PAGE.

Если **код операции** — мксдкоп \_ Set \_ S0PAGE \_ Resource:

-   Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит из структуры **escape-заголовка мксдк \_ \_ \_ T** и структуры [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) , Объединенной в структуру [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .
-   Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен осуществляться между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), но между вызовами **StartPage** и **EndPage** может быть несколько таких вызовов.
-   Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с мксдкоп \_ Set \_ S0PAGE \_ Resource как **код операции** для каждого ресурса на странице, прежде чем вызывать его с мксдкоп \_ Set \_ S0PAGE.

Когда **код операции** — мксдкоп \_ Set \_ кспспасссру \_ mode:

-   Параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) состоит только из структуры **escape-заголовка мксдк \_ \_ \_ T** .
-   Этот вызов должен быть выполнен до вызова [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

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

 

