---
description: Метод размещения \_ addressType задает тип адреса.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: 'Итконнектион: метод ut_AddressType:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675225"
---
# <a name="itconnectionput_addresstype-method"></a>Итконнектион: \_ метод AddressType:p UT

\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **размещения \_ addressType** задает тип адреса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паддресстипе* \[ окне\]
</dt> <dd>

Указатель на **строку BSTR** , содержащую тип адреса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                                   | Описание                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод успешно выполнен.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *паддресстипе* .<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для выполнения операции.<br/> |
| <dl> <dt>**\_Ошибка E**</dt> </dl>        | Незаданная ошибка.<br/>                                   |
| <dl> <dt>**E \_ нотимпл**</dt> </dl>     | Этот метод еще не реализован.<br/>                  |



 

## <a name="remarks"></a>Комментарии

Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Паддресстипе* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Header<br/>       | <dl> <dt>Сдпблб. h</dt> </dl>   |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итконнектион**](itconnection.md)
</dt> <dt>

[**Итконнектион:: получение \_ addressType**](itconnection-get-addresstype.md)
</dt> </dl>

 

