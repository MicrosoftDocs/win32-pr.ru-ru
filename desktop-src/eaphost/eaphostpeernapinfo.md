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
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071940"
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

## <a name="remarks"></a>Комментарии

Структура **еафостпирнапинфо** предшествует [стрингкоррелатионид](/windows/desktop/NAP/nap-datatypes) NAP типа данных **WCHAR** в потоке байтов RPC.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                   |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Еафостпирапис. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры запрашивающего сторона EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**еафостпиржетаусстатус**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**еафостпирмесодауспарамс**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

