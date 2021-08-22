---
title: XTYP_ADVSTOPная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип адвстоп для завершения цикла рекомендаций с сервером. функция обратного вызова сервера платформа динамических данных Exchange (DDE), ддекаллбакк, получает эту транзакцию, когда клиент указывает кстип \_ адвстоп в функции ддеклиенттрансактион.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP данных транзакций Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81f1fe407186410e604a259f6e8039c074da039fc23b2f8a090c34ff58154
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544773"
---
# <a name="xtyp_advstop-transaction"></a>\_Транзакция кстип адвстоп

Клиент использует транзакцию **кстип \_ адвстоп** для завершения цикла рекомендаций с сервером. функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **кстип \_ адвстоп** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*утипе* 
</dt> <dd>

Тип транзакции.

</dd> <dt>

*уфмт* 
</dt> <dd>

Формат данных, связанный с завершенным циклом рекомендаций.

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

Не используется.

</dd> <dt>

*dwData1* 
</dt> <dd>

Не используется.

</dd> <dt>

*dwData2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Failed \_ advise** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**ддепостадвисе**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Зрения**
</dt> <dt>

[библиотека управления Exchange платформа динамических данных](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

