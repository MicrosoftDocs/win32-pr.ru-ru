---
description: 'Иенумусеридентити:: Skip не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'Метод Иенумусеридентити:: Skip (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997667"
---
# <a name="ienumuseridentityskip-method"></a>Метод Иенумусеридентити:: Skip

\[**Иенумусеридентити:: Skip** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Пропускает заданное число интерфейсов удостоверения пользователя в перечислении. Используется при извлечении интерфейсов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*celt* \[ окне\]
</dt> <dd>

Тип: **ulong**

Число интерфейсов, которые нужно пропустить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Примечания

[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь. Чтобы увеличить это число без извлечения интерфейсов, вызовите этот метод. Чтобы сбросить счетчик, вызовите метод [**иенумусеридентити:: Reset**](ienumuseridentity-reset.md).

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

[**Иенумусеридентити:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**Иенумусеридентити:: Next**](ienumuseridentity-next.md)
</dt> <dt>

[**Иенумусеридентити:: NOCOUNT**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




