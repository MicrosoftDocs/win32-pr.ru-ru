---
title: XTYP_DISCONNECTная транзакция (Ддемл. h)
description: функция обратного вызова ддекаллбакк платформа динамических данных приложения Exchange (DDE) получает \_ транзакцию отключения кстип, когда участник приложения в диалоге использует функцию ддедисконнект для завершения диалога.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- XTYP_DISCONNECT данных транзакций Exchange
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8763ba9eda7782bff21a9abdedc3c99672ad927bdd7944181391802f9378497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914781"
---
# <a name="xtyp_disconnect-transaction"></a>КСТИП \_ Отключить транзакцию

функция обратного вызова [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)платформа динамических данных приложения Exchange (DDE) получает транзакцию **\_ отключения кстип** , когда участник приложения в диалоге использует функцию [**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) для завершения диалога.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Маркер для того, что диалог был завершен.

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

Не используется.

</dd> <dt>

*dwData1* 
</dt> <dd>

Не используется.

</dd> <dt>

*dwData2* 
</dt> <dd>

Указывает, являются ли участники диалога одним и тем же экземпляром приложения. Если этот параметр равен 1, то партнеры являются одним и тем же экземпляром. Если этот параметр равен 0, то участники являются разными экземплярами.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта транзакция фильтруется, если приложение указало флаг **КБФ \_ Skip \_ unconnected** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Приложение может получить состояние прерванного диалога, вызвав функцию [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) при обработке этой транзакции. После возврата функции обратного вызова этот обработчик станет недействительным.

Приложение не может блокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>ддемл. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**Зрения**
</dt> <dt>

[библиотека управления Exchange платформа динамических данных](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

