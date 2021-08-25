---
description: Windows Инструментарий управления (WMI) определяет набор системных свойств, связанных со всеми классами и экземплярами классов.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Свойства системы WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3471665e2e818037bb831c8d8ab39bbe0d56e01912afb1a3399b4055d3670a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120664"
---
# <a name="wmi-system-properties"></a>Свойства системы WMI

Windows Инструментарий управления (WMI) определяет набор системных свойств, связанных со всеми классами и экземплярами классов. Как и системные классы, имена системных свойств начинаются с двойного символа подчеркивания, что отличает их от свойств, созданных приложениями или поставщиками, которые не должны начинаться с одинарной или двойной подчеркивания. Другой способ указать системное свойство — использовать метод [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

Системные свойства доступны в любое время, но значения могут быть **равны NULL**. **Значение NULL** указывает, что свойство не применимо к конкретному объекту. Однако свойства системы могут быть недоступными все время для всех классов или экземпляров.

## <a name="system-properties"></a>Свойства системы

В следующем списке описываются свойства системы WMI. Приведенные примеры взяты из системных свойств класса [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , который описан в нижней части этого раздела.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_См**
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения для экземпляров; чтение и запись для классов

Имя класса.

Пример: Win32 \_ оптионалфеатуре

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Рожден**
</dt> <dd>

Тип данных: **массив \_ строк CIM**

Тип доступа: только для чтения для экземпляров и классов

Иерархия классов текущего класса или экземпляра. Первый элемент является непосредственным родительским классом, далее — родительским и т. д. последний элемент является базовым классом.

Пример: {CIM \_ логикалелемент, CIM \_ манажедсистемелемент}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Династию**
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения

Имя класса верхнего уровня, от которого производятся экземпляры класса или экземпляра. Если этот класс или экземпляр является классом верхнего уровня, значения **\_ \_ династию** и **\_ \_ Class** одинаковы.

Пример: CIM \_ манажедсистемелемент

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_женус**
</dt> <dd>

Тип данных: **CIM \_ SINT32**

Тип доступа: только для чтения

Значение, используемое для различения классов и экземпляров. Это значение является **\_ \_ классом WBEM женус** (1) для классов и **\_ \_ экземпляром WBEM женус** (2) для экземпляров и событий.

Пример: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Имен**](--namespace.md)
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения

Имя [*пространства имен*](gloss-n.md) класса или экземпляра.

Пример: root \\ CIMV2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Путь**
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения

Полный путь к классу или экземпляру, включая сервер и пространство имен.

Пример: \\ \\ MyServer \\ root \\ CIMV2: Win32 \_ Оптионалфеатуре. Name = "телнетклиент"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_\_Число свойств**
</dt> <dd>

Тип данных: **CIM \_ SINT32**

Тип доступа: только для чтения

Количество несистемных свойств, определенных для класса или экземпляра.

Пример: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_релпас**
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения

Относительный путь к классу или экземпляру.

Пример: Win32 \_ оптионалфеатуре. Name = "телнетклиент"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Сервером**
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения

Имя сервера, предоставляющего класс или экземпляр.

Пример: MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Суперкласс**
</dt> <dd>

Тип данных: **\_ строка CIM**

Тип доступа: только для чтения

Имя непосредственный родительский класс класса или экземпляра.

Пример: CIM \_ логикалелемент

</dd> </dl>

Следующий код PowerShell извлекает свойства класса [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , который включает в себя свойства системы.


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



Предыдущий пример кода возвращает следующее:


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
