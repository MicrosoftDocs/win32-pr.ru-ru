---
title: Сложный тип Евентдефинитионтипе
description: Определяет событие, которое может записывать поставщик.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- Журнал событий сложных типов Евентдефинитионтипе
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691960"
---
# <a name="eventdefinitiontype-complex-type"></a>Сложный тип Евентдефинитионтипе

Определяет событие, которое может записывать поставщик.

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Имя</th>
<th>Тип</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>channel</td>
<td>token</td>
<td>Идентификатор, определяющий канал, на который записывается событие. Укажите идентификатор канала одного из определенных или импортированных каналов. Если канал не указывает идентификатор канала, используйте имя канала. Дополнительные сведения об определении или импорте канала см. в описании сложного типа <a href="eventmanifestschema-channellisttype-complextype.md"><strong>чаннеллисттипе</strong></a> .<br/> Если канал не указан, событие не записывается в канал. Как правило, единственной причиной, по которой не нужно указывать канал, является запись событий только в сеанс ETW. Дополнительные сведения см. в разделе Управление сеансами <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">трассировки событий</a>Windows.<br/></td>
</tr>
<tr class="even">
<td>keywords</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>кнамелист</strong></a></td>
<td>Разделенный пробелами список имен ключевых слов, которые определяют категорию событий, к которым относится это событие. Укажите имя ключевого слова из списка определяемых вами ключевых слов. Дополнительные сведения об определении ключевых слов см. в описании сложного типа <a href="eventmanifestschema-keywordtype-complextype.md"><strong>кэйвордтипе</strong></a> .<br/> Если не указать ключевые слова, то дескриптор события будет содержать ноль для ключевых слов.<br/></td>
</tr>
<tr class="odd">
<td>уровень</td>
<td><strong>QName</strong></td>
<td>Уровень детализации, используемый при записи события. Укажите имя уровня, определенного в манифесте, или одного из уровней, определенных в \Include\Winmeta.xml файле, включенном в Windows SDK. Дополнительные сведения об определении уровня см. в разделе сложный тип <a href="eventmanifestschema-leveltype-complextype.md"><strong>левелтипе</strong></a> .<br/> Если уровень не указан, дескриптор события будет содержать ноль для Level.<br/> Необходимо указать уровень, если тип канала, на который записано событие, — Admin; уровень должен быть одним из следующих уровней, определенных в Winmeata.xml:
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>стртаблереф</strong></a></td>
<td>Локализованное сообщение для события. Строка сообщения ссылается на локализованную строку в разделе " <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> " манифеста.<br/> Необходимо указать сообщение, если тип канала, на который написано событие, — admin.<br/></td>
</tr>
<tr class="odd">
<td>нотлогжед</td>
<td>Логическое</td>
<td>Определяет, регистрирует ли поставщик это событие. Укажите значение true, если поставщик регистрирует это событие; в противном случае — значение false. Используйте этот атрибут, чтобы указать, что поставщик больше не регистрирует это событие вместо удаления события из манифеста. При хранении события в манифесте пользователи смогут декодировать старые ETL-файлы, включающие событие.<br/> <strong>Windows Server 2008 и Windows Vista:</strong> Этот атрибут не поддерживается в версиях компилятора сообщений, поставляемых до версии Windows 7 Windows SDK.<br/></td>
</tr>
<tr class="even">
<td>транслируют</td>
<td><strong>QName</strong></td>
<td>Имя кода операции, определяющего операцию в задаче. Укажите имя кода операции, определенного в манифесте, или одного из кодов операций, определенных в Winmeta.xml. Дополнительные сведения об определении кода операции см. в разделе сложный тип <a href="eventmanifestschema-opcodetype-complextype.md"><strong>опкодетипе</strong></a> .<br/> Если задача, на которую указывает ссылка, содержит операции (локальные) для конкретных задач, можно указать один из его специфических кодов задач или код операции, определенный на уровне поставщика (Глобальный код операции). При указании глобального кода операции значение глобального кода операции не может совпадать с одним из локальных кодов операций для задачи.<br/> Если вы ссылаетесь на локальный код операции, атрибут Task должен ссылаться на задачу, которой принадлежит локальный код операции.<br/> Если не указать код операции, то дескриптор события будет содержать ноль для кода операции.<br/></td>
</tr>
<tr class="odd">
<td>символ</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>ксимболтипе</strong></a></td>
<td>Символ, используемый для ссылки на дескриптор события для этого события в приложении. <a href="message-compiler--mc-exe-.md"><strong>Компилятор сообщений (MC.exe)</strong></a> использует символ, чтобы создать константу для дескриптора события в файле заголовка, создаваемом компилятором. Если не указать символ, компилятор создаст его. Дескриптор используется при вызове функции <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> для записи события.<br/></td>
</tr>
<tr class="even">
<td>задача</td>
<td><strong>QName</strong></td>
<td>Имя задачи, определяющей компонент или подкомпонент, который создает это событие. Укажите имя задачи, определенной в манифесте. Дополнительные сведения об определении задачи см. в описании сложного типа <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .<br/> Если задача не указана, то дескриптор события будет содержать ноль для задачи.<br/></td>
</tr>
<tr class="odd">
<td>шаблон</td>
<td>token</td>
<td>Идентификатор шаблона шаблона, который определяет элементы данных, включаемые в это событие. Укажите идентификатор шаблона, определенного в манифесте. Дополнительные сведения об определении шаблона см. в разделе сложный тип <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>темплатеитемтипе</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>значение</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></td>
<td>Идентификатор события. Идентификатор должен быть уникальным в пределах списка определяемых вами событий.<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>Однобайтовый номер версии определения события.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Если для форматирования строки сообщения для события используется [**евтформатмессаже**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) (или Просмотр событий для просмотра строки сообщения), строка сообщения может содержать строки вставки и любые строки формата, поддерживаемые функцией Win32 **FormatMessage** . Строки вставки ограничены%*n* или%*n*! s! (например, %1), где *n* — это односторонняя ссылка на элементы данных, определенные в шаблоне события. Строка сообщения также может содержать строки вставки параметров в форме%%*n* (например,% %4). Максимальное число строк вставки, которое может содержать сообщение, — 100.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

