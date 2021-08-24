---
title: Перечисление Контролреконнектстатус
description: Указывает результат метода повторного подключения IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Контролреконнектстатус
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635adbcafd5180dad967e2488b793f6907fd38cc848935a088bee59aad536354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738084"
---
# <a name="controlreconnectstatus-enumeration"></a>Перечисление Контролреконнектстатус

Указывает результат метода [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**контролреконнектстартед**
</dt> <dd>

Операция повторного подключения была запущена.

</dd> <dt>

<span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**контролреконнектблоккед**
</dt> <dd>

Не удалось запустить операцию повторного подключения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





