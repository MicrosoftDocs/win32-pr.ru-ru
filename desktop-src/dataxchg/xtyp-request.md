---
title: XTYP_REQUESTная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию запроса кстип для запроса данных с сервера. Функция обратного вызова сервера платформа динамических данных Exchange (DDE), Ддекаллбакк, получает эту транзакцию, когда клиент указывает \_ запрос кстип в функции ддеклиенттрансактион.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- XTYP_REQUEST обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801396"
---
# <a name="xtyp_request-transaction"></a>\_Транзакция запроса кстип

Клиент использует транзакцию **\_ запроса кстип** для запроса данных с сервера. Функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **\_ запрос кстип** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*утипе* 
</dt> <dd>

Тип транзакции.

</dd> <dt>

*уфмт* 
</dt> <dd>

Формат, в котором сервер должен отправлять данные клиенту.

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

Сервер должен вызвать функцию [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) для создания маркера данных, определяющего данные, а затем возвращающего маркер. Сервер должен вернуть **значение NULL** , если не удается завершить транзакцию. Если сервер возвращает **значение NULL**, клиент получит \_ флаг DDE фнотпроцессед.

## <a name="remarks"></a>Комментарии

Эта транзакция фильтруется, если серверное приложение указало флаг " **КБФ \_ сбой \_ запросов** " в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Если ответ на эту транзакцию требует длительной обработки, сервер может вернуть \_ код возврата блока CBR, чтобы приостановить будущие транзакции в текущем диалоге, а затем обработать транзакцию асинхронно. Когда сервер завершит работу и данные готовы к передаче клиенту, сервер может вызвать функцию [**ддинаблекаллбакк**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) для возобновления диалога.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>Ддемл. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**ддинаблекаллбакк**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека управления платформа динамических данных Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

