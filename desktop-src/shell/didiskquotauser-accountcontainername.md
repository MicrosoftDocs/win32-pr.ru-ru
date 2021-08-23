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
ms.openlocfilehash: a7a439fe36262e7f73fd7b839fd60af5b1b0a9b05f77769ab1d6a8c5ee9d06fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094239"
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

## <a name="remarks"></a>Remarks

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

 

 




