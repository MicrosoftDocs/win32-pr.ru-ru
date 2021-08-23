---
description: Сбрасывает внутреннее число извлеченных интерфейсов в перечислении.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'Метод Иенумусеридентити:: Reset (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: df70048760af47b380308eddab4ef5c044c8f6881374c83002944d6d76836ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969423"
---
# <a name="ienumuseridentityreset-method"></a>Метод Иенумусеридентити:: Reset

\[**Иенумусеридентити:: Reset** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Сбрасывает внутреннее число извлеченных интерфейсов в перечислении.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь. Вызов этого метода приведет к сбросу значения этого счетчика.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                         |
| Заголовок<br/>                   | <dl> <dt>Мсидент. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсидент. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иенумусеридентити**](ienumuseridentity.md)
</dt> <dt>

[**Иенумусеридентити:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**Иенумусеридентити:: NOCOUNT**](ienumuseridentity-getcount.md)
</dt> <dt>

[**Иенумусеридентити:: Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




