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
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843355"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дидисккуотаусер**](didiskquotauser-object.md)
</dt> </dl>

 

 




