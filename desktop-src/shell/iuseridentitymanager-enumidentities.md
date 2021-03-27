---
description: 'Иусеридентитиманажер:: Енумидентитиес не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Метод Иусеридентитиманажер:: Енумидентитиес (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143027"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>Метод Иусеридентитиманажер:: Енумидентитиес

\[**Иусеридентитиманажер:: енумидентитиес** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Возвращает объект [**иенумусеридентити**](ienumuseridentity.md) , который можно использовать для перечисления удостоверений пользователей, имеющихся в системе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенумусер* \[ заполняет\]
</dt> <dd>

Тип: **[ **иенумусеридентити**](ienumuseridentity.md)\*\***

Адрес указателя на новый объект перечисления идентификаторов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Результат операции извлечения. В случае успеха возвращается значение S \_ ОК. Если не удалось создать объект перечисления, он возвращает E \_ OUTOFMEMORY.

## <a name="remarks"></a>Примечания

Этот метод полезен для итерации по списку удостоверений в системе. Чтобы получить одиночное удостоверение с помощью файла cookie, не обращаясь к списку, вызовите [**иусеридентитиманажер:: жетидентитибикукие**](iuseridentitymanager-getidentitybycookie.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсидент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иусеридентитиманажер**](iuseridentitymanager.md)
</dt> <dt>

[**иенумусеридентити**](ienumuseridentity.md)
</dt> <dt>

[**Иусеридентитиманажер:: Жетидентитибикукие**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




