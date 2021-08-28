---
description: Ниже перечислены квалификаторы, используемые для определения классов поставщиков представления.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Квалификаторы, относящиеся к поставщику представления
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7890effa0e8edd07edbb9506f88a78ceffc65fcb8d19bf6c8bcf67860a677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130976"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Квалификаторы, относящиеся к поставщику представления

Ниже перечислены квалификаторы, используемые для определения классов поставщиков представления.

> [!Note]  
> Класс поставщика представления поддерживает только NetBIOS-имена при использовании удаленных ссылок. Если в удаленной ссылке используется IP-адрес или имя DNS, соединение завершается с ошибкой 0x800706BA.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Направлений**
</dt> <dd>

Тип данных: **логический**

Используется со свойствами сопоставления представлений для предотвращения сопоставления ссылок на представление со ссылками на представления.

В следующем примере свойство **GroupComponent** определяется как ссылка на ассоциацию, которая не сопоставлена со ссылкой на представление.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**хиддендефаулт**
</dt> <dd>

Тип данных: **логический**

Значение по умолчанию для свойства класса представления на основе свойства исходного класса с другим значением по умолчанию. Базовый класс источника подразумевается представлением.

Например, исходный класс [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) имеет [логическое](boolean.md) свойство **рунрепеатедли** , которое указывает, должно ли задание выполняться периодически или только один раз. Значение по умолчанию **рунрепеатедли** не равно true для **Win32 \_ ScheduledJob**, но имеет значение true для класса View.


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**жоинон**
</dt> <dd>

Тип данных: **строка**

Определяет, как присоединяются экземпляры исходного класса в классах представления соединения. В следующем примере показано, как использовать квалификатор **жоинон** для объединения двух исходных классов.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**месодсаурце**
</dt> <dd>

Тип данных: **массив строк**

Исходный метод для выполнения метода представления. Аналогичные инструкции см. в разделе [квалификатор пропертисаурцес](propertysources-qualifier.md). Сигнатура метода должна точно соответствовать сигнатуре исходного класса. Скопируйте сигнатуру метода из MOF-файла, определяющего исходный класс. В приведенном ниже примере определяется метод из метода [**клеаревентлог**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) в [**Win32 \_ нтевентлогфиле**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Этот квалификатор допустим только в том случае, если он используется с представлениями Union.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**постжоинфилтер**](postjoinfilter-qualifier.md)
</dt> <dd>

Тип данных: **строка**

WQL-запрос для фильтрации экземпляров после их соединения в классе соединения.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**пропертисаурцес**](propertysources-qualifier.md)
</dt> <dd>

Тип данных: **массив строк**

Исходные свойства, из которых свойство класса представления получает данные.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**Наборов**
</dt> <dd>

Тип данных: **логический**

Указывает, определяется ли класс объединения. Представления Union содержат экземпляры, основанные на объединении исходных экземпляров. Например, вы можете объявить следующее:


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**виевсаурцес**](viewsources-qualifier.md)
</dt> <dd>

Тип данных: **массив строк**

Набор запросов язык запросов WMI (WQL), определяющих исходные экземпляры и свойства, используемые в определенном классе представления. Важность соответствия всех квалификаторов массива важна.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**виевспацес**](viewspaces-qualifier.md)
</dt> <dd>

Тип данных: **массив строк**

Пространства имен, в которых находятся исходные экземпляры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



 

