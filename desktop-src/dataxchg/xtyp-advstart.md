---
title: XTYP_ADVSTARTная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип адвстарт для установки цикла рекомендаций с сервером.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART данных транзакций Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544763"
---
# <a name="xtyp_advstart-transaction"></a>\_Транзакция кстип адвстарт

Клиент использует транзакцию **кстип \_ адвстарт** для установки цикла рекомендаций с сервером. функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **кстип \_ адвстарт** в качестве параметра *wType* функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*утипе* 
</dt> <dd>

Тип транзакции.

</dd> <dt>

*уфмт* 
</dt> <dd>

Формат данных, запрашиваемый клиентом.

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

## <a name="return-value"></a>Возвращаемое значение

Функция обратного вызова сервера должна возвращать **значение true** , чтобы разрешить цикл рекомендаций по заданному имени раздела и паре имен элементов, или **false** для запрета цикла рекомендаций. Если функция обратного вызова возвращает **значение true**, любые последующие вызовы функции [**ддепостадвисе**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) на сервере с тем же именем раздела и парой имен элементов приводят к тому, что система отправляет транзакции [**кстип \_ Адврек**](xtyp-advreq.md) на сервер.

## <a name="remarks"></a>Remarks

если клиент запрашивает цикл рекомендаций по имени раздела, имени элемента и формату данных для уже установленного цикла рекомендаций, то библиотека платформа динамических данных Exchange Management Library (ддемл) не создает дублирующий цикл рекомендаций, а изменяет флаги цикла рекомендаций (**кстипф \_ аккрек** и **кстипф \_ NODATA**) в соответствии с последним запросом.

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

 

