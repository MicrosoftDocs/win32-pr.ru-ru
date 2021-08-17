---
title: Имстскаксевентс Онсервицемессажерецеивед, метод
description: Вызывается, когда клиент получает системное сообщение.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онсервицемессажерецеивед
- Службы удаленных рабочих столов метода Онсервицемессажерецеивед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онсервицемессажерецеивед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca511710834f8aa9fdda02565c33c4732e4cba9300e74ad3b48276d74890bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757252"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a>Метод Имстскаксевентс:: Онсервицемессажерецеивед

Вызывается, когда клиент получает системное сообщение.

## <a name="syntax"></a>Синтаксис


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сервицемессаже* \[ окне\]
</dt> <dd>

Указывает системное сообщение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Дополнительные сведения о системных сообщениях см. [в статье Настройка обмена сообщениями для удаленный рабочий стол сервера шлюза](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

