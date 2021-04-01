---
title: Тфклиентид (Мсктф. h)
description: Тип данных Тфклиентид используется для обнаружения клиента.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- тфклиентид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801805"
---
# <a name="tfclientid"></a>тфклиентид

Тип данных **тфклиентид** используется для обнаружения клиента.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Комментарии

В TSF приложения и текстовые службы обычно называются клиентами. Каждый клиент получает уникальный идентификатор, который используется для идентификации при вызове различных методов диспетчера TSF. Этот идентификатор имеет тип **тфклиентид** .

Тип данных **тфклиентид** предоставляется диспетчером TSF. Приложение получает значение **тфклиентид** при вызове [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate). Значение Тфклиентид для службы текстового ввода передается методу [итфтекстинпутпроцессор:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) . Любой объект, который не соответствует указанным выше категориям, может получить идентификатор клиента путем вызова [итфклиентид:: ClientID](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Приложения Windows 2000 Professional \[ классические приложения \| UWP\]<br/>                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows 2000 \|\]<br/>                          |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                      |
| Header<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Итфклиентид:: ClientId**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**Итфтекстинпутпроцессор:: Activate**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr:: Activate**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





