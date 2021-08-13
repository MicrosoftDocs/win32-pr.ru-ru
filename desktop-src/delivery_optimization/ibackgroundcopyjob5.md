---
title: Интерфейс IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Этот интерфейс используется для запроса или установки нескольких необязательных поведений задания.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Интерфейс IBackgroundCopyJob5
- Интерфейс IBackgroundCopyJob5, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 593f06f74dde7e6891417871cd16dc3730ef005fb90a0a1b6cf5377fda7ebcd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461974"
---
# <a name="ibackgroundcopyjob5-interface"></a>Интерфейс IBackgroundCopyJob5

Этот интерфейс используется для запроса или установки нескольких необязательных поведений задания.

Чтобы получить этот интерфейс, вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** , используя в `__uuidof(IBackgroundCopyJob5)` качестве идентификатора интерфейса.

## <a name="members"></a>Элементы

Интерфейс **IBackgroundCopyJob5** наследует от [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IBackgroundCopyJob5** содержит следующие методы.



| Метод                                                 | Описание                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Универсальный метод для получения свойств задания.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Универсальный метод для настройки свойств задания.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 определяется как E847030C-БББА-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





