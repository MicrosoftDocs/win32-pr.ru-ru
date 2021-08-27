---
title: Свойство ConnectionOptions. UserName (Всмандисп. h)
description: Задает и возвращает имя пользователя локальной или доменной учетной записи на удаленном компьютере. Это свойство определяет имя пользователя для проверки подлинности.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства имени пользователя
- свойство UserName служба удаленного управления Windows, объект ConnectionOptions
- служба удаленного управления Windows объекта ConnectionOptions, свойство UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fa4cd5e1d4fd733431adab80241744c0b197960506cfe2908bc99315ecfdea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121784"
---
# <a name="connectionoptionsusername-property"></a>ConnectionOptions. UserName, свойство

Задает и возвращает имя пользователя локальной или доменной учетной записи на удаленном компьютере. Это свойство определяет имя пользователя для проверки подлинности. Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Значение свойства

Строка, содержащая имя локального пользователя или учетной записи домена на удаленном компьютере.

Если значение не указано, а флаг **всманфлагкредусернамепассворд** не установлен, используется имя пользователя учетной записи, на которой работает скрипт.

Если значение не указано и установлен флаг **всманфлагкредусернамепассворд** , сценарий предлагает пользователю ввести имя пользователя и пароль. Если допустимое имя пользователя и пароль не указаны, возвращается ошибка отказа в доступе.

## <a name="remarks"></a>Remarks

Для указания этого свойства используется следующий синтаксис.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



Вы можете указать **имя пользователя** и [**пароль**](connectionoptions-password.md) для учетной записи домена при использовании проверки подлинности [*Negotiate*](windows-remote-management-glossary.md) или *Kerberos* или для локальной учетной записи с [*обычной*](windows-remote-management-glossary.md) проверкой подлинности. Для подключения к локальной учетной записи флаги [**WSMan. CreateSession**](wsman-createsession.md) должны содержать сочетание флага **всманфлагусебасик** и флага **всманфлагкредусернамепассворд** . Для подключения к доменной учетной записи флаги **WSMan. CreateSession** должны содержать сочетание флага **всманфлагусенеготиате** и флага **всманфлагкредусернамепассворд** , а также сочетание флага **всманфлагусекерберос** и флага **всманфлагкредусернамепассворд** . Для учетной записи домена **имя пользователя** должно быть указано в формате " \\ имя пользователя компьютера", где часть строки может быть либо именем, либо IP-адресом. Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Для подключения к доменной учетной записи флаги [**WSMan. CreateSession**](wsman-createsession.md) должны содержать сочетание флага **всманфлагусенеготиате** и флага **всманфлагкредусернамепассворд** для подключения к учетной записи домена, для которой требуется проверка подлинности Negotiate.


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a>Требования



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

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





