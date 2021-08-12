---
title: Структура Еафостпирнапинфо (Еафостпирапис. h)
description: Содержит сведения о защите доступа к сети (NAP) по запрашивающему сторона EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Еафостпирнапинфо структура EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fe91c88f633f2e42599938e45e1291c90f1ec9c08559a84f132f3af9269de39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274543"
---
# <a name="eaphostpeernapinfo-structure"></a>Структура Еафостпирнапинфо

Структура **еафостпирнапинфо** содержит сведения о защите доступа к сети (NAP) на запрашивающем сторона EAP.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>Члены

<dl> <dt>

**исолатионстате**
</dt> <dd>

Структура [**\_ состояния изоляции**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) , указывающая состояние изоляции NAP компьютера. Состояние изоляции определяет уровень предоставляемого доступа к сети.

</dd> <dt>

**пробатионтиме**
</dt> <dd>

Структура **пробатионтиме** , указывающая время, необходимое для выхода из карантина, после которого соединение будет удалено. Структура **пробатионтиме** идентична структуре [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> <dt>

**стрингкоррелатионидленгс**
</dt> <dd>

Длина [СТРИНГКОРРЕЛАТИОНИД](/windows/desktop/NAP/nap-datatypes) NAP в байтах, которая соответствует этой структуре.

</dd> </dl>

## <a name="remarks"></a>Remarks

Структура **еафостпирнапинфо** предшествует [стрингкоррелатионид](/windows/desktop/NAP/nap-datatypes) NAP типа данных **WCHAR** в потоке байтов RPC.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                   |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                      |
| Заголовок<br/>                   | <dl> <dt>Еафостпирапис. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры запрашивающего сторона EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**еафостпиржетаусстатус**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**еафостпирмесодауспарамс**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

