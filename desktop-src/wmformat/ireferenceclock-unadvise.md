---
title: Иреференцеклокк метод unadvise
description: Метод unadvise отменяет запрос уведомления.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Метод Unadvise для Windows Media Format
- Метод Unadvise для Windows Media Format, интерфейс Иреференцеклокк
- Иреференцеклокк интерфейса Windows Media Format, метод unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133239"
---
# <a name="ireferenceclockunadvise-method"></a>Метод Иреференцеклокк:: unadvise

Метод **unadvise** отменяет запрос уведомления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двадвисекукие* 
</dt> <dd>

Идентификатор удаляемого запроса. Используйте значение, возвращаемое функцией Адвисетиме, в параметре Пдвадвисекукие.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                             | Описание                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Метод выполнен успешно.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | Переданный идентификатор не существует.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иреференцеклокк**](ireferenceclock.md)
</dt> </dl>

 

 





