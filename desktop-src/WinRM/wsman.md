---
title: Объект WSMan (Всмандисп. h)
description: Предоставляет методы и свойства, используемые для создания сеанса, представленного объектом Session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Объект WSMan служба удаленного управления Windows
- Объект WSMan служба удаленного управления Windows, описание
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414877"
---
# <a name="wsman-object"></a>Объект WSMan

Предоставляет методы и свойства, используемые для создания сеанса, представленного объектом [**Session**](session.md) . Любой служба удаленного управления Windows операции требует создания [**сеанса**](session.md) , который подключается к удаленному компьютеру, [*базовому контроллеру управления*](windows-remote-management-glossary.md) (BMC) или локальному компьютеру. К операциям относятся получение, запись, перечисление или вызов методов.

## <a name="members"></a>Элементы

Объект **WSMan** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **WSMan** содержит следующие методы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Метод</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createconnectionoptions.md"><strong>креатеконнектионоптионс</strong></a></td>
<td style="text-align: left;">Создает объект <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> , который указывает имя пользователя и пароль, используемые при создании удаленного сеанса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-createresourcelocator.md"><strong>креатересаурцелокатор</strong></a></td>
<td style="text-align: left;">Создает объект <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> , который может указывать:<br/>
<ul>
<li>Полный путь к <a href="windows-remote-management-glossary.md"><em>ресурсу</em></a> или отдельному фрагменту данных.</li>
<li><a href="windows-remote-management-glossary.md"><em>Селектор</em></a> для конкретного экземпляра ресурса.</li>
<li><a href="windows-remote-management-glossary.md"><em>Параметр</em></a> , предоставляющий дополнительные данные поставщику ресурсов.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></td>
<td style="text-align: left;">Создает объект <a href="session.md"><strong>сеанса</strong></a> , который затем может использоваться для последующих сетевых операций.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. Енумератионфлагхиерарчидип</strong></a></td>
<td style="text-align: left;">Возвращает значение флага перечисления <strong>енумератионфлагхиерарчидип</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. Енумератионфлагхиерарчидипбасепропсонли</strong></a></td>
<td style="text-align: left;">Возвращает значение флага перечисления <strong>енумератионфлагхиерарчидипбасепропсонли</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. Енумератионфлагхиерарчишаллов</strong></a></td>
<td style="text-align: left;">Возвращает значение флага перечисления <strong>енумератионфлагхиерарчишаллов</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. Енумератионфлагнонксмлтекст</strong></a></td>
<td style="text-align: left;">Возвращает значение константы перечисления <strong>всманфлагнонксмлтекст</strong> для использования в параметре <em>flags</em> метода <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. Енумератионфлагретурнепр</strong></a></td>
<td style="text-align: left;">Возвращает значение флага перечисления <strong>енумератионфлагретурнепр</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. Енумератионфлагретурнобжект</strong></a></td>
<td style="text-align: left;">Возвращает значение флага перечисления <strong>енумератионфлагретурнобжект</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. Енумератионфлагретурнобжектандепр</strong></a></td>
<td style="text-align: left;">Возвращает значение флага перечисления <strong>енумератионфлагретурнобжектандепр</strong> для использования в параметре <em>flags</em> <a href="session-enumerate.md"><strong>сеанса. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-geterrormessage.md"><strong>WSMan. Жетеррормессаже</strong></a></td>
<td style="text-align: left;">Возвращает отформатированную строку, содержащую текст номера ошибки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. Сессионфлагкредусернамепассворд</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагкредусернамепассворд</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. Сессионфлаженаблеспнсерверпорт</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлаженаблеспнсерверпорт</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. Сессионфлагноенкриптион</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагноенкриптион</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. Сессионфлагскипкачекк</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагскипкачекк</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. Сессионфлагскипкнчекк</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагскипкнчекк</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. Сессионфлагусебасик</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагусебасик</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. Сессионфлагуседижест</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагуседижест</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. Сессионфлагусекерберос</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагусекерберос</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. Сессионфлагусенеготиате</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагусенеготиате</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. Сессионфлагусеноаусентикатион</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>всманфлагусеноаусентикатион</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></td>
<td style="text-align: left;">Возвращает значение флага проверки подлинности <strong>WSManFlagUTF8</strong> для использования в параметре <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Свойства

Объект **WSMan** имеет следующие свойства.



| Свойство                                            | Тип доступа          | Описание                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**Команд**](wsman-commandline.md)<br/> | Только для чтения<br/> | Возвращает необработанную командную строку для текущего ведущего процесса.<br/> |
| [**Ошибка**](wsman-error.md)<br/>             | Только для чтения<br/> | Возвращает сведения об ошибке.<br/>                                            |



 

## <a name="remarks"></a>Комментарии

Объект **WSMan** соответствует интерфейсам [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) и [**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) . **WSMan** — это единственный объект, который можно создать напрямую с помощью функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Примеры

В следующем примере кода показано, как создать экземпляр объекта **WSMan** .


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[API сценариев WinRM](winrm-scripting-api.md)
</dt> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

