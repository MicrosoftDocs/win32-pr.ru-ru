---
description: Получить или изменить данные реестра можно с помощью класса Стдрегпров WMI и его методов.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Получение данных реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701343"
---
# <a name="obtaining-registry-data"></a>Получение данных реестра

Получить или изменить данные реестра можно с помощью класса [**СТДРЕГПРОВ**](/previous-versions/windows/desktop/regprov/stdregprov) WMI и его методов. При использовании программы Regedit для просмотра и изменения значений реестра на локальном компьютере **стдрегпров** позволяет использовать сценарий или приложение для автоматизации таких действий на локальном компьютере и на удаленных компьютерах.

[**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) содержит методы для следующих задач:

-   Проверка прав доступа для пользователя
-   Создание, перечисление и удаление разделов реестра
-   Создание, перечисление и удаление подразделов или именованных значений
-   Чтение, запись и удаление значений данных

Данные реестра упорядочены по поддеревьям, ключам и подразделам, вложенным в ключ верхнего уровня. Фактические значения данных называются записями или именованными значениями.

К поддеревьям относятся следующие:

-   **HKey \_ \_Корень классов** (сокращенно, как **HKCR**)
-   **HKey \_ ТЕКУЩИЙ \_ пользователь** (**HKCU**)
-   **HKey \_ ЛОКАЛЬНЫЙ \_ компьютер** (**HKLM**)
-   **\_Пользователи hKey**
-   **\_Текущая \_ Конфигурация hKey**

Например, в записи реестра **hKey** \\ **Software** \\ **Microsoft** \\ **DirectX** \\ **инсталледверсион**, поддерево hKey — это **программное обеспечение**, подразделы — **Microsoft** и **DirectX**, а запись именованного значения — **инсталледверсион**.

[**Регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) возникает, когда происходит изменение определенного ключа, но запись не определяет, как изменяются значения, а это событие не активируется изменениями ниже указанного ключа. Для определения изменений в любом месте иерархии ключевой структуры используйте [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), который не возвращает определенные значения или изменения ключа. Чтобы получить определенное изменение значения записи, используйте [**события registryvaluechangeevent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), а затем прочтите запись, чтобы получить базовое значение.

[**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) содержит только методы, которые могут вызываться из C++ или скрипта, который отличается от структуры классов Win32.

В следующем примере кода показано, как использовать метод [**стдрегпров. енумкэй**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) для перечисления всех подразделов программного обеспечения Майкрософт в разделе реестра.

**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Майкрософт**


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





[**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) имеет различные методы для чтения различных типов данных значений записей реестра. Если запись имеет неизвестные значения, то для их перечисления можно вызвать метод [**стдрегпров. енумвалуес**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) . В следующей таблице перечислены соответствия между методами **стдрегпров** и типами данных.



| Метод                                                                                  | Тип данных           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**жетбинаривалуе**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **\_двоичный файл REG**     |
| [**жетдвордвалуе**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**жетекспандедстрингвалуе**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **\_распаковать \_ SZ** |
| [**жетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ Multi \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

В следующей таблице перечислены соответствующие методы для создания новых ключей или значений, а также изменения существующих.



| Метод                                                                                  | Тип данных           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**сетбинаривалуе**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **\_двоичный файл REG**     |
| [**сетдвордвалуе**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**сетекспандедстрингвалуе**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **\_распаковать \_ SZ** |
| [**сетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ Multi \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

В следующем примере показано, как прочитать список источников для журнала системных событий из раздела реестра.

**HKey \_ \_** \\  \\  \\  \\ **Система журнала событий** \\  служб, установленная в системе локального компьютера

Обратите внимание, что элементы в многострочном значении обрабатываются как коллекция или массив.


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



Поставщик реестра размещается в локальной службе, а не на LocalSystem. Поэтому получение сведений удаленно из поддерева **hKey \_ текущий \_ пользователь** невозможно. Однако сценарии, выполняемые на локальном компьютере, по-прежнему могут обращаться к **\_ текущему \_ пользователю hKey**. Можно задать для модели размещения значение LocalSystem на удаленном компьютере, но это является угрозой безопасности, так как реестр на удаленном компьютере уязвим для злонамеренного доступа. Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).

## <a name="examples"></a>Примеры

Пример кода на языке VBScript в [разделе "чтение двоичного значения реестра](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) " в коллекции TechNet использует инструментарий WMI для чтения двоичного значения реестра.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Задачи WMI: реестр](wmi-tasks--registry.md)
</dt> </dl>

 

 
