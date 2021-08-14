---
title: XTYP_REGISTERная транзакция (Ддемл. h)
description: функция обратного вызова платформа динамических данных Exchange (DDE) получает \_ тип транзакции REGISTER кстип каждый раз, когда серверное приложение платформа динамических данных библиотеки управления Exchange (ддемл) использует функцию дденамесервице для регистрации имени службы или в случае, когда запускается приложение, не являющееся ддемл, которое поддерживает системный раздел.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER данных транзакций Exchange
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544753"
---
# <a name="xtyp_register-transaction"></a>КСТИП \_ зарегистрировать транзакцию

функция обратного вызова платформа динамических данных Exchange (DDE) получает тип транзакции **\_ REGISTER кстип** каждый [*раз, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)серверное приложение платформа динамических данных библиотеки управления Exchange (ддемл) использует функцию [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для регистрации имени службы или в случае, когда запускается приложение, не являющееся ддемл, которое поддерживает системный раздел.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Регистрируемое имя базовой службы.

</dd> <dt>

*hsz2* 
</dt> <dd>

Регистрация регистрируемого имени службы для конкретного экземпляра.

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

Эта транзакция фильтруется, если приложение указало флаг **КБФ \_ пропустить \_ регистрации** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Приложение не может блокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.

Приложение должно использовать параметр *hsz1* , чтобы добавить имя службы в список серверов, доступных пользователю. Приложение должно использовать параметр *hsz2* для указания того, какой экземпляр приложения запущен.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>ддемл. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Зрения**
</dt> <dt>

[библиотека управления Exchange платформа динамических данных](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

