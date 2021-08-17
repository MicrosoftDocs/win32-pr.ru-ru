---
title: XTYP_POKEная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип, чтобы отправить незапрошенные данные на сервер. функция обратного вызова сервера платформа динамических данных Exchange (DDE), ддекаллбакк, получает эту транзакцию, когда клиент указывает кстип \_ в функции ддеклиенттрансактион.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE данных транзакций Exchange
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a179f4130ae06c4548b52586d6086201c2d832a158cef877d9aaf524160f4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914754"
---
# <a name="xtyp_poke-transaction"></a>КСТИП \_ Вставка транзакции

Клиент использует транзакцию **кстип \_** , чтобы отправить незапрошенные данные на сервер. функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **кстип \_** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*утипе* 
</dt> <dd>

Тип транзакции.

</dd> <dt>

*уфмт* 
</dt> <dd>

Формат данных, отправляемых с сервера.

</dd> <dt>

*хконв* 
</dt> <dd>

Обработчик диалога.

</dd> <dt>

*hsz1* 
</dt> <dd>

Маркер имени раздела.

</dd> <dt>

*hsz2* 
</dt> <dd>

Маркер имени элемента.

</dd> <dt>

*хдата* 
</dt> <dd>

Обработчик данных, отправляемых клиентом на сервер.

</dd> <dt>

*dwData1* 
</dt> <dd>

Не используется.

</dd> <dt>

*dwData2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция обратного вызова сервера должна возвращать флаг **DDE \_ факк** , если он обрабатывает эту транзакцию, флаг **DDE \_ фбуси** , если он слишком занят для обработки этой транзакции, или флаг **\_ фнотпроцессед DDE** , если он отклоняет эту транзакцию.

## <a name="remarks"></a>Remarks

Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ \_ Failed** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>ддемл. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Зрения**
</dt> <dt>

[библиотека управления Exchange платформа динамических данных](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

