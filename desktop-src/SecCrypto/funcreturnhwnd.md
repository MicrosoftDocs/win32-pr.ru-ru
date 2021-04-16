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
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664407"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Кспдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кпаккуиреконтекст**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**втаблепровструк**](vtableprovstruc.md)
</dt> </dl>

 

 
