---
description: Обработчик для объекта локальной политики.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Нтсекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080843"
---
# <a name="lsa_handle"></a>LSA \_ Handle

Тип **данных \_ обработчика LSA** — это обработчик локального объекта [**политики**](policy-object.md) .


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Комментарии

Прежде чем использовать интерфейс локальной политики API, приложение должно открыть обработчик для объекта [**политики**](policy-object.md) . Для этого вызовите [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Эта функция возвращает маркер, который приложение может указать в последующих вызовах функции политики LSA.

Каждый обработчик имеет связанный набор разрешений, определяющий операции, которые приложение может выполнять над объектом [**политики**](policy-object.md) с помощью этого маркера. Приложение может одновременно открыть более одного маркера для объекта **политики** . Если маркер больше не требуется, приложение должно закрыть его, вызвав [**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Нтсекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

