---
title: Имстскаксевентс Онидлетимеаутнотификатион, метод
description: Вызывается, когда пользователь не наводит мышь или клавиатуру в течение периода времени, заданного \_ методом имсрдпклиентадванцедсеттингс минутестоидлетимеаут.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онидлетимеаутнотификатион
- Службы удаленных рабочих столов метода Онидлетимеаутнотификатион, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онидлетимеаутнотификатион
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672725"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>Метод Имстскаксевентс:: Онидлетимеаутнотификатион

Вызывается, когда пользователь не наводит мышь или клавиатуру в течение периода времени, заданного методом [**имсрдпклиентадванцедсеттингс::p UT \_ минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .

## <a name="syntax"></a>Синтаксис


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

По умолчанию значение свойства [**минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) равно нулю, и система не отслеживает время ожидания простоя. Это событие возникает, только если свойству присвоено ненулевое значение.

Значение параметра [**минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) автоматически сбрасывается каждый раз при возникновении события.

Приложения могут использовать [**минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) в ситуациях, когда полезно отключать пользователя; Например, в режиме киоска или в другом открытом сценарии терминала.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





