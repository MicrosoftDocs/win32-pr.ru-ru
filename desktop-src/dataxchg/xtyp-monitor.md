---
title: XTYP_MONITORная транзакция (Ддемл. h)
description: Функция обратного вызова DDE в отладчике платформа динамических данных Exchange (DDE), Ддекаллбакк, получает \_ транзакцию монитора кстип при каждом возникновении в системе события DDE.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415309"
---
# <a name="xtyp_monitor-transaction"></a>\_Транзакция монитора кстип

Функция обратного вызова DDE в отладчике платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), Получает транзакцию **\_ монитора кстип** при каждом возникновении в системе события DDE. Чтобы получить эту транзакцию, приложение должно указать значение **\_ монитора APPCLASS** при вызове функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*утипе* 
</dt> <dd>

Тип транзакции.

</dd> <dt>

*уфмт* 
</dt> <dd>

Не используется.

</dd> <dt>

*хконв* 
</dt> <dd>

Не используется.

</dd> <dt>

*hsz1* 
</dt> <dd>

Не используется.

</dd> <dt>

*hsz2* 
</dt> <dd>

Не используется.

</dd> <dt>

*хдата* 
</dt> <dd>

Маркер объекта DDE, который содержит сведения о событии DDE. Приложение должно использовать функцию [**ддеакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) для получения указателя на объект.

</dd> <dt>

*dwData1* 
</dt> <dd>

Не используется.

</dd> <dt>

*dwData2* 
</dt> <dd>

Событие DDE. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                      | Значение                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ ОБРАТные вызовы**</dt> <dt>0x08000000</dt> </dl> | Система послала транзакцию функции обратного вызова DDE. Объект DDE содержит структуру [**монкбструкт**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) , которая предоставляет сведения о транзакции.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_**</dt> <dt>0x40000000</dt> </dl>                | Сеанс DDE был установлен или прерван. Объект DDE содержит структуру [**монконвструкт**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) , которая предоставляет сведения о диалоге.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ ОШИБКИ**</dt> <dt>0x10000000</dt> </dl>          | Произошла ошибка DDE. Объект DDE содержит структуру [**монеррструкт**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) , которая предоставляет сведения об ошибке.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ ХСЗ \_ info**</dt> <dt>0x01000000</dt> </dl>   | Приложение DDE, которое было создано, освобождено или увеличило число использований строкового маркера, или маркер строки был освобожден в результате вызова функции [**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . Объект DDE содержит структуру [**монхсзструкт**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) , которая предоставляет сведения о строковом маркере.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ ССЫЛКИ**</dt> <dt>0x20000000</dt> </dl>             | Приложение DDE запустило или остановило цикл рекомендаций. Объект DDE содержит структуру [**монлинкструкт**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) , которая предоставляет сведения о цикле рекомендаций.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_ ПОСТМСГС**</dt> <dt>0x04000000</dt> </dl>    | Система или приложение разместили сообщение DDE. Объект DDE содержит структуру [**монмсгструкт**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) , которая предоставляет сведения о сообщении.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ СЕНДМСГС**</dt> <dt>0x02000000</dt> </dl>    | Система или приложение отправили сообщение DDE. Объект DDE содержит структуру [**монмсгструкт**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) , которая предоставляет сведения о сообщении.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция обратного вызова обрабатывает эту транзакцию, она должна возвращать значение 0.

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

[**ддеакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**монкбструкт**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**монконвструкт**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**монеррструкт**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**монхсзструкт**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**монлинкструкт**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**монмсгструкт**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека управления платформа динамических данных Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

