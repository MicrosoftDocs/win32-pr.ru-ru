---
title: Объект ConnectionOptions (Всмандисп. h)
description: Объект ConnectionOptions передается методу CreateSession для предоставления имени пользователя и пароля, связанных с локальной учетной записью на удаленном компьютере.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта ConnectionOptions
- служба удаленного управления Windows объекта ConnectionOptions, описание
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8665dc3a5be91fddb4332be3512ec9eec5c483495a21b95b641ec26e4e9e111
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734094"
---
# <a name="connectionoptions-object"></a>Объект ConnectionOptions

Объект **ConnectionOptions** передается методу [**CreateSession**](wsman-createsession.md) для предоставления имени пользователя и пароля, связанных с локальной учетной записью на удаленном компьютере. Если параметры не указаны, то для учетных данных, в которых выполняется скрипт, задаются значения по умолчанию.

## <a name="members"></a>Элементы

Объект **ConnectionOptions** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Объект **ConnectionOptions** имеет следующие свойства.



| Свойство                                                  | Тип доступа           | Описание                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Пароль**](connectionoptions-password.md)<br/> | Только на запись<br/> | Задает пароль локальной или доменной учетной записи на удаленном компьютере.<br/>           |
| [**Имен**](connectionoptions-username.md)<br/> | Чтение/запись<br/> | Задает и возвращает имя пользователя локальной или доменной учетной записи на удаленном компьютере.<br/> |



 

## <a name="remarks"></a>Remarks

Объект **ConnectionOptions** соответствует интерфейсу [**ивсманконнектионоптионс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .

если клиентское приложение служба удаленного управления Windows выполняется под олицетворением, то при установке свойства [**Password**](connectionoptions-password.md) происходит сбой. Клиентское приложение — это сценарий или другая программа, которая отправляет запрос в службу WinRM на локальном или удаленном компьютере. Клиентское приложение может работать под олицетворением, так как оно называется функцией, например [**имперсонатеклиент**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)). Страница Active Server (ASP) или служба не может запрашивать имя пользователя и пароль, если процесс ASP выполняется с учетной записью, выполняющей олицетворение клиента.

Флаг **всманфлагкредусернамепассворд** должен быть установлен для вызова [**WSman. CreateSession**](wsman-createsession.md) при использовании [**имени пользователя**](connectionoptions-username.md) и [**пароля**](connectionoptions-password.md) для проверки подлинности.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript показано, как создать объект **ConnectionOptions** , задать свойства учетной записи на удаленном компьютере и использовать его при создании объекта [**Session**](session.md) .


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Проверка подлинности для удаленных подключений](authentication-for-remote-connections.md)
</dt> <dt>

[API сценариев WinRM](winrm-scripting-api.md)
</dt> <dt>

[о служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

