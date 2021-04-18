---
description: '\_Тип данных обработчика сцесвк — это непрозрачный маркер, предоставляемый набором средств настройки безопасности.'
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (Сцесвк. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540975"
---
# <a name="scesvc_handle"></a>СЦЕСВК, \_ обработчик

Тип **данных \_ обработчика сцесвк** — это непрозрачный маркер, предоставляемый набором средств настройки безопасности. Он используется методами интерфейсов [**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) и [**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) для передачи информации между оснасткой настройки безопасности и расширением оснастки.


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Сцесвк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исцесвкаттачментдата**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[**исцесвкаттачментперсистинфо**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




