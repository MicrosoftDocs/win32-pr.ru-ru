---
description: Используется поставщиком служб шифрования (CSP) для получения маркера окна, который CSP должен использовать в качестве родительского или владельца любого отображаемого пользовательского интерфейса.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: Указатель функции CRYPT_RETURN_HWND (Кспдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 387e1e9140dac8081acf851eb7125a612506783adbeefe1174137ff7f74fae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006752"
---
# <a name="crypt_return_hwnd-function-pointer"></a>\_Функция шифрования возвращает \_ указатель функции HWND

Функция обратного вызова **функретурнхвнд** используется [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для получения маркера окна, который CSP должен использовать в качестве родительского или владельца любого отображаемого пользовательского интерфейса.

## <a name="syntax"></a>Синтаксис


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ФВНД* \[ в, out\]
</dt> <dd>

Адрес переменной **HWND** , которая получает дескриптор родительского окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот указатель функции не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Кспдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кпаккуиреконтекст**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**втаблепровструк**](vtableprovstruc.md)
</dt> </dl>

 

 
