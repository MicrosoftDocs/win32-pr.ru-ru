---
title: XTYP_CONNECT_CONFIRMная транзакция (Ддемл. h)
description: функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает \_ \_ транзакцию кстип CONNECT CONFIRM, чтобы подтвердить, что диалог был установлен с клиентом, и предоставить серверу этот обработчик диалога.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM данных транзакций Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0259540801a49bc631dc60e33979a8730b46bdfc06ac81142098e851b8a51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499092"
---
# <a name="xtyp_connect_confirm-transaction"></a>КСТИП \_ подключение \_ подтвердить транзакцию

функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает транзакцию **кстип \_ CONNECT \_ CONFIRM** [*, чтобы*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)подтвердить, что диалог был установлен с клиентом, и предоставить серверу этот обработчик диалога. Система отправляет эту транзакцию в результате предыдущей транзакции [**кстип \_ Connect**](xtyp-connect.md) или [**кстип \_ вилдконнект**](xtyp-wildconnect.md) .


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Маркер нового диалога.

</dd> <dt>

*hsz1* 
</dt> <dd>

Маркер имени раздела, в котором было установлено диалоговое обсуждение.

</dd> <dt>

*hsz2* 
</dt> <dd>

Маркер имени службы, для которого было установлено диалоговое обсуждение.

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

Указывает, является ли клиент тем же экземпляром приложения, что и сервер. Если параметр равен 1, то клиент является тем же экземпляром. Если параметр равен 0, то клиент является другим экземпляром.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Skip \_ Connect \_** для функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Сервер не может заблокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>ддемл. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Зрения**
</dt> <dt>

[библиотека управления Exchange платформа динамических данных](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

