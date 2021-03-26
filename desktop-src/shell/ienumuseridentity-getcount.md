---
description: Функция NOCOUNT не поддерживается и может быть изменена или недоступна в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Метод Иенумусеридентити:: NOCOUNT (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345385"
---
# <a name="ienumuseridentitygetcount-method"></a>Метод Иенумусеридентити:: NOCOUNT

\[Функция **NOCOUNT** не поддерживается и может быть изменена или недоступна в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Возвращает число удостоверений пользователей, находящихся в системе в настоящее время.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнкаунт* \[ заполняет\]
</dt> <dd>

Тип: **ulong \** _

Указатель на _ *ulong**, получающий счетчик.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Примечания

Если поддержка нескольких удостоверений пользователей отключена, *пнкаунт* получит значение 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсидент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумусеридентити**](ienumuseridentity.md)
</dt> <dt>

[**Иенумусеридентити:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**Иенумусеридентити:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**Иенумусеридентити:: Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




