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
ms.openlocfilehash: 3e37f2b786d32ab9f42738e6a8522c6f4593aa6b21a490a6fdd969233b4a6dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888173"
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

## <a name="remarks"></a>Remarks

**Унсубскрибесервицечанженотификатионс** не возвращает, пока не будут завершены необработанные Обратные вызовы в процессе. Поэтому нельзя вызвать **унсубскрибесервицечанженотификатионс** в обратном вызове, не вызывая взаимоблокировки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                   |
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

 

 




