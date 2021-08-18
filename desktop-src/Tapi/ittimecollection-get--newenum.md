---
description: 'Метод Иттимеколлектион:: get__NewEnum — метод Get \_ \_ NewEnum Возвращает перечислитель для коллекции.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'Метод Иттимеколлектион:: get__NewEnum (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ba76f1d10e2cb9ee937ec688af3e87e0bb9310df9fc39afaef64e60ea55b1dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991904"
---
# <a name="ittimecollectionget__newenum-method"></a>Метод Иттимеколлектион:: Get \_ \_ NewEnum

\[встречи и элементы управления встречными IP-телефонными соединениями недоступны для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Get \_ \_ NewEnum** Возвращает перечислитель для коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ заполняет\]
</dt> <dd>

Указатель на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) в объекте перечислителя для коллекции.

Вызовите метод [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на возвращенном интерфейсе **IUnknown** , чтобы получить указатель на интерфейс перечисления [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) в коллекции. **IEnumVARIANT** предоставляет ряд методов, которые можно использовать для итерации по коллекции.

Дополнительные сведения см. в разделе "Примечания".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                                   | Описание                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод успешно выполнен.<br/>                                    |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Параметр *Pval* не является допустимым указателем.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для выполнения операции.<br/> |
| <dl> <dt>**\_Ошибка E**</dt> </dl>        | Незаданная ошибка.<br/>                                   |
| <dl> <dt>**E \_ нотимпл**</dt> </dl>     | Этот метод еще не реализован.<br/>                  |



 

## <a name="remarks"></a>Remarks

Этот метод является взаимозаменяемым с [**Get \_ енумератиониф**](ittimecollection-get-enumerationif.md) , за исключением того, что он возвращает **IUnknown** вместо [**иенумтиме**](ienumtime.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Заголовок<br/>       | <dl> <dt>Сдпблб. h</dt> </dl>   |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иттимеколлектион**](ittimecollection.md)
</dt> <dt>

[**иттиме**](ittime.md)
</dt> </dl>

 

