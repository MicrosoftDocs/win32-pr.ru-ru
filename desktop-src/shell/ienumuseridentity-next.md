---
description: 'Иенумусеридентити:: Next не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Метод Иенумусеридентити:: Next (Мсидент. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb3074a7b55ce03e7372491fce11160f1df1bc5fc8a4e45ad0f12d4538d4b2f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009404"
---
# <a name="ienumuseridentitynext-method"></a>Метод Иенумусеридентити:: Next

\[**Иенумусеридентити:: Next** не поддерживается и может быть изменен или недоступен в будущем. Вместо этого используйте [учетные записи пользователей с быстрым переключением пользователей и удаленный рабочий стол](fastuserswitching.md).\]

Не рекомендуется. Извлекает из перечисления массив интерфейсов удостоверения пользователя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*celt* \[ окне\]
</dt> <dd>

Тип: **ulong**

Значение типа **ulong** , представляющее число получаемых интерфейсов.

</dd> <dt>

*rgelt* \[ заполняет\]
</dt> <dd>

Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Адрес указателя, получающего интерфейсы.

</dd> <dt>

*пцелтфетчед* \[ заполняет\]
</dt> <dd>

Тип: **ulong \***

Адрес указателя, который получает число успешно извлеченных интерфейсов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

[**Иенумусеридентити**](ienumuseridentity.md) хранит внутренний счетчик, указывающий, какой интерфейс следует извлечь. Несколько вызовов этого метода не будут сбрасывать это число. Чтобы сбросить счетчик, вызовите метод [**иенумусеридентити:: Reset**](ienumuseridentity-reset.md). Чтобы увеличить число без извлечения интерфейсов, вызовите [**иенумусеридентити:: Skip**](ienumuseridentity-skip.md).

Значение параметра *celt* не должно превышать значение, возвращенное [**Иенумусеридентити:: NOCOUNT**](ienumuseridentity-getcount.md).

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

[**Иенумусеридентити:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**Иенумусеридентити:: NOCOUNT**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
