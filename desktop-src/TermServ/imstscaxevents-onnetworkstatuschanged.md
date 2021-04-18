---
title: Имстскаксевентс Оннетворкстатусчанжед, метод
description: Вызывается при изменении состояния сети. | Имстскаксевентс Оннетворкстатусчанжед, метод
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Оннетворкстатусчанжед
- Службы удаленных рабочих столов метода Оннетворкстатусчанжед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Оннетворкстатусчанжед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674581"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>Метод Имстскаксевентс:: Оннетворкстатусчанжед

Вызывается при изменении состояния сети.

## <a name="syntax"></a>Синтаксис


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*куалитилевел* \[ окне\]
</dt> <dd>

Указывает новую скорость подключения. Это может быть одно из следующих значений.

<dt>

1
</dt> <dd>

Менее 512 килобайт в секунду (кбит/с).

</dd> <dt>

2
</dt> <dd>

512 – 1 999 кбит/с.

</dd> <dt>

3
</dt> <dd>

2 000 – 9 999 кбит/с.

</dd> <dt>

4
</dt> <dd>

Больше или равно 10 000 кбит/с.

</dd> </dl> </dd> <dt>

*пропускная способность* \[ окне\]
</dt> <dd>

Указывает пропускную способность подключения.

</dd> <dt>

*RTT* \[ окне\]
</dt> <dd>

Указывает задержку подключения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





