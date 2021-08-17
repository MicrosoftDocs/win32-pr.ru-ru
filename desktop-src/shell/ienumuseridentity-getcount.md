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
ms.openlocfilehash: e4848ec183096b37adbc04521fab04fd800d3783377d1e14b3abd068819648ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678941"
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

Тип: **ulong \***

Указатель на **ulong** , получающая счетчик.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если поддержка нескольких удостоверений пользователей отключена, *пнкаунт* получит значение 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                         |
| Заголовок<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
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

 

 




