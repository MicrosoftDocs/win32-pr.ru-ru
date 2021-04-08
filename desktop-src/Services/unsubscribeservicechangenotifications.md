---
description: Отменяет подписывание уведомлений об изменении состояния службы.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Функция Унсубскрибесервицечанженотификатионс (Винсвкп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911244"
---
# <a name="unsubscribeservicechangenotifications-function"></a>Функция Унсубскрибесервицечанженотификатионс

Отменяет подписывание уведомлений об изменении состояния службы. Эта функция использует подписки, возвращаемые функцией [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md).

## <a name="syntax"></a>Синтаксис


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псубскриптион* \[ окне\]
</dt> <dd>

Указатель на подписку, для которой необходимо отменить подписку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

**Унсубскрибесервицечанженотификатионс** не возвращает, пока не будут завершены необработанные Обратные вызовы в процессе. Поэтому нельзя вызвать **унсубскрибесервицечанженотификатионс** в обратном вызове, не вызывая взаимоблокировки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Винсвкп. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md)
</dt> <dt>

[**куерисервицединамиЦинформатион**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




