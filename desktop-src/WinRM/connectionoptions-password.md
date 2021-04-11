---
title: Свойство ConnectionOptions. Password (Всмандисп. h)
description: Задает пароль локальной или доменной учетной записи на удаленном компьютере. Это свойство определяет пароль для проверки подлинности.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Свойство пароля служба удаленного управления Windows
- Свойство Password служба удаленного управления Windows, объект ConnectionOptions
- Служба удаленного управления Windows объекта ConnectionOptions, свойство Password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136503"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions. Password, свойство

Задает пароль локальной или доменной учетной записи на удаленном компьютере. Это свойство определяет пароль для проверки подлинности. Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>Значение свойства

Строка, содержащая пароль локальной или доменной учетной записи на удаленном компьютере.

Если значение не указано, а флаг **всманфлагкредусернамепассворд** не установлен, используется пароль учетной записи, в которой работает скрипт.

Если значение не указано и установлен флаг **всманфлагкредусернамепассворд** , сценарий предлагает пользователю ввести пароль (и имя пользователя, если оно не указано). Если допустимое имя пользователя и пароль не указаны, возвращается ошибка отказа в доступе.

## <a name="remarks"></a>Комментарии

Имейте в виду, что вы не можете получить пароль. Пароль можно задать только с помощью этого свойства.

Если вы создаете объект [**ConnectionOptions**](connectionoptions.md) и используете имя пользователя и пароль для подключения к служба удаленного управления Windows, установите флаг **Всманфлагкредусернамепассворд** для вызова [**WSMan. CreateSession**](wsman-createsession.md).

Дополнительные сведения о настройке паролей см. в разделе "Примечания" в [**ConnectionOptions**](connectionoptions.md).

## <a name="examples"></a>Примеры

В следующем примере кода создается объект [**ConnectionOptions**](connectionoptions.md) и задается **пароль**.


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
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

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





