---
description: Возвращает имя контейнера учетной записи пользователя.
title: Дидисккуотаусер. Аккаунтконтаинернаме, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808819"
---
# <a name="didiskquotauseraccountcontainername-property"></a>Дидисккуотаусер. Аккаунтконтаинернаме, свойство

Возвращает имя контейнера учетной записи пользователя.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Значение свойства

Строковое значение, заданное для имени контейнера учетной записи пользователя.

## <a name="remarks"></a>Примечания

Для учетных записей без сведений о службах каталогов это свойство содержит имя домена. Для учетных записей со сведениями о службах каталогов это свойство содержит каноническое имя с удаленным именем завершающего объекта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дидисккуотаусер**](didiskquotauser-object.md)
</dt> </dl>

 

 




