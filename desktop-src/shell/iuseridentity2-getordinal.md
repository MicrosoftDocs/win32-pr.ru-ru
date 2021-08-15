---
description: Параметр ordinal не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'Метод IUserIdentity2:: метода ordinal (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d5453a083a1db23e042d24c3da4cd2948ff70f813fcc9026a00324eade467918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968973"
---
# <a name="iuseridentity2getordinal-method"></a>Метод IUserIdentity2:: метода Ordinal

\[Параметр **Ordinal** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Возвращает порядковый номер этого удостоверения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двординал* \[ заполняет\]
</dt> <dd>

Тип: **DWORD \***

Указатель на значение **DWORD** , которое получает порядковый номер для этого удостоверения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Порядковый номер определяет порядок удостоверений в списке удостоверений, но может не сохраняться во всех операциях с удостоверениями. Чтобы получить уникальное значение для удостоверения, вызовите метод [**Кука**](iuseridentity-getcookie.md).

## <a name="requirements"></a>Requirements (Требования)



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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetCookie**](iuseridentity-getcookie.md)
</dt> </dl>

 

 




