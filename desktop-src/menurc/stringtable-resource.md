---
title: Ресурс STRINGTABLE
description: Определяет один или несколько строковых ресурсов для приложения. Строковые ресурсы — это просто заканчивающиеся нулем строки в Юникоде или ASCII, которые можно загрузить при необходимости из исполняемого файла с помощью функции Лоадстринг.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Меню ресурсов STRINGTABLE и другие ресурсы
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133862"
---
# <a name="stringtable-resource"></a>Ресурс STRINGTABLE

Определяет один или несколько строковых ресурсов для приложения. Строковые ресурсы — это просто заканчивающиеся нулем строки в Юникоде или ASCII, которые можно загрузить при необходимости из исполняемого файла с помощью функции [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa) .

Существует два способа форматирования оператора **STRINGTABLE** :

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- или -

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*Необязательные операторы*
</dt> <dd>

Этот параметр может быть равен нулю или нескольким следующим операторам.



| Инструкция                                                        | Описание                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Параметры**](characteristics-statement.md) *DWORD*     | Определяемая пользователем информация о ресурсе, который может использоваться средствами чтения и записи файлов ресурсов. Дополнительные сведения см. в разделе [**характеристики**](characteristics-statement.md). |
| [](language-statement.md) *Язык* языка, *подязык* | Указывает язык ресурса. Дополнительные сведения см. в разделе [**Language**](language-statement.md).                                                                              |
| [**Версия**](version-statement.md) *DWORD*                     | Определяемый пользователем номер версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов. Дополнительные сведения см. в разделе [**версия**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

16-разрядное целое число без знака, идентифицирующее ресурс.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*Строка*
</dt> <dd>

Одна или несколько строк, заключенных в кавычки. Длина строки не должна превышать 4097 символов и должна занимать одну строку в исходном файле. Чтобы добавить в строку символ возврата каретки, используйте следующую последовательность символов: \\ 012. Например, строка «одна \\ 012Line две» определяет строку, которая отображается следующим образом:

``` syntax
Line one
Line two
```

Чтобы внедрить кавычки в строку, используйте следующую последовательность: "". Например, строка "" "третьего типа" "" определяет строку, которая отображается следующим образом:

``` syntax
"Line three"
```

Для кодирования символов Юникода используется символ "L", за которым следуют символы Юникода, заключенные в кавычки. Пример см. в разделе "примеры".

Компилятор ресурсов также поддерживает продолжение строк в *строке*. Пример см. в разделе "примеры".

</dd> </dl>

Для обратной совместимости также поддерживаются некоторые атрибуты. Дополнительные сведения см. в разделе [Общие атрибуты ресурсов](common-resource-attributes.md).

## <a name="remarks"></a>Комментарии

Версия-кандидат выделяет 16 строк на раздел и использует значение идентификатора, чтобы определить, какой раздел должен содержать строку. Строки, идентификаторы которых отличаются только нижними 4 битами, помещаются в один раздел. Дополнительные сведения см. в разделе [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Примеры

В следующем примере показано использование оператора **STRINGTABLE** для вывода строк ASCII:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

В следующем примере показано, как кодировать символы Юникода:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

В следующем примере показаны строки с кодировкой ASCII и Юникод. Обратите внимание, что строки без начального символа "L" используют формат escape-последовательности из двух цифр:

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

В следующем примере показано, как можно использовать продолжения строки:

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**Accelerator**](accelerators-resource.md)
</dt> <dt>

[**ПОКАЗАТЕЛИ**](characteristics-statement.md)
</dt> <dt>

[**ЯЗЫКЕ**](language-statement.md)
</dt> <dt>

[**МЕНЮ**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Версия**](version-statement.md)
</dt> </dl>

 

 