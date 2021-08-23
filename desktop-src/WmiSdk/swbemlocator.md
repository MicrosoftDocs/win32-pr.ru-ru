---
description: Методы объекта SWbemLocator можно использовать для получения объекта SWbemServices, который представляет соединение с пространством имен на локальном или удаленном компьютере.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Объект SWbemLocator (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0e93e9bd0bfb33c495b30afbde47bcb9b007acb4cd00dece42e1a8c3b88e99d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732795"
---
# <a name="swbemlocator-object"></a>Объект SWbemLocator

Методы объекта **SWbemLocator** можно использовать для получения объекта [**SwbemServices**](swbemservices.md) , который представляет соединение с пространством имен на локальном или удаленном компьютере. Затем можно использовать методы объекта **SwbemServices** для доступа к WMI. Этот объект может быть создан вызовом метода **CreateObject** VBScript.

## <a name="members"></a>Элементы

Объект **SWbemLocator** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **SWbemLocator** содержит эти методы.



| Метод                                              | Описание                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**коннектсервер**](swbemlocator-connectserver.md) | Подключается к инструментарию WMI на указанном компьютере.<br/> |



 

### <a name="properties"></a>Свойства

Объект **SWbemLocator** имеет следующие свойства.



| Свойство                                                | Тип доступа          | Описание                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Безопасность\_**](swbemlocator-security-.md)<br/> | Только для чтения<br/> | Используется для чтения или изменения параметров безопасности.<br/> |



 

## <a name="remarks"></a>Remarks

В верхней части объектной модели библиотеки сценариев WMI находится объект SWbemLocator. SWbemLocator используется для установления подключения с проверкой подлинности к пространству имен WMI, точно так же, как функция VBScript GetObject и моникер WMI "винмгмтс:" используются для установления подключения к WMI с проверкой подлинности. Однако SWbemLocator предназначен для выполнения двух конкретных сценариев сценариев, которые не могут быть выполнены с помощью GetObject и моникера WMI. SWbemLocator необходимо использовать, если необходимо:

-   Укажите учетные данные пользователя и пароль для подключения к инструментарию WMI на удаленном компьютере. Моникер WMI, используемый с функцией GetObject, не включает механизм для указания учетных данных. Для большинства действий WMI (включая все, что выполняется на удаленных компьютерах) требуются права администратора. Если обычно используется обычная учетная запись пользователя, а не учетная запись администратора, то выполнение большинства задач WMI будет невозможным, если не запустить сценарий в разделе альтернативные учетные данные.
-   Подключение wmi, если на веб-странице выполняется сценарий wmi. Нельзя использовать функцию GetObject при выполнении скриптов, внедренных в HTML-страницу, так как Internet Explorer запрещает использование GetObject в целях безопасности.

Кроме того, можно использовать SWbemLocator для подключения к инструментарию WMI, если найдена строка подключения WMI, используемая с GetObject, запутанной или сложной.

Для создания ссылки на SWbemLocator используется CreateObject, а не GetObject. Чтобы создать ссылку, необходимо передать функции CreateObject программный идентификатор SWbemLocator (ProgID) "Вбемскриптинг. SWbemLocator", как показано в строке 2 в следующем примере скрипта. После получения ссылки на объект SWbemLocator вызывается метод Коннектсервер для подключения к WMI и получения ссылки на объект SWbemServices. Это продемонстрировано в строке 3 следующего сценария.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Чтобы выполнить сценарий с дополнительными учетными данными, укажите имя пользователя и пароль в качестве дополнительных параметров, передаваемых в Коннектсервер. Например, этот сценарий выполняется с учетными данными пользователя с именем кенмер с паролем хомерж.


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



\\Для указания имени пользователя также можно использовать формат имени пользователя домена. Пример:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Примеры

В следующем примере PowerShell для подключения к серверу используется **SWbemLocator** .


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | IID \_ исвбемлокатор<br/>                                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

 




