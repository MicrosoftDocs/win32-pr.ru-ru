---
title: Перечисление Контролклосестатус
description: Указывает, может ли приложение, содержащее элемент управления, немедленно закрыть элемент управления.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Контролклосестатус
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988288"
---
# <a name="controlclosestatus-enumeration"></a>Перечисление Контролклосестатус

Указывает, может ли приложение, содержащее элемент управления, немедленно закрыть элемент управления.

## <a name="syntax"></a>Синтаксис


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**контролклосеканпроцеед**
</dt> <dd>

Контейнер может немедленно закрываться. Это может произойти, если элемент управления не подключен.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**контролклосеваитфоревентс**
</dt> <dd>

Контейнер должен ожидать событий [**имстскаксевентс:: Ondisconnectо**](imstscaxevents-ondisconnected.md) или [**Имстскаксевентс:: онконфирмклосе**](imstscaxevents-onconfirmclose.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                      |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имсрдпклиент:: RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**Имстскаксевентс:: Онконфирмклосе**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**Имстскаксевентс:: ondisconnectо**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





