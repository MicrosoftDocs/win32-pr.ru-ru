---
title: Интерфейс Ибаккграундкопикаллбакк (Deliveryoptimization. h)
description: Реализуйте интерфейс Ибаккграундкопикаллбакк, чтобы получить уведомление о завершении задания, его изменении или об ошибке. Клиенты используют этот интерфейс вместо опроса состояния задания.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Интерфейс Ибаккграундкопикаллбакк
- Интерфейс Ибаккграундкопикаллбакк, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165a1edcdb6bd70de8fad379fcc89d5afc36776348fd7751277614229a23377e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953644"
---
# <a name="ibackgroundcopycallback-interface"></a>Интерфейс Ибаккграундкопикаллбакк

Реализуйте интерфейс **ибаккграундкопикаллбакк** , чтобы получить уведомление о завершении задания, его изменении или об ошибке. Клиенты используют этот интерфейс вместо опроса состояния задания.

## <a name="members"></a>Элементы

Интерфейс **ибаккграундкопикаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ибаккграундкопикаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ибаккграундкопикаллбакк** содержит следующие методы.



| Метод                                                                    | Описание                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**жоберрор**](ibackgroundcopycallback-joberror-method.md)               | Вызывается при возникновении ошибки.<br/>                                           |
| [**жобмодификатион**](ibackgroundcopycallback-jobmodification-method.md) | Вызывается при изменении задания.<br/>                                         |
| [**жобтрансферред**](ibackgroundcopycallback-jobtransferred.md)          | Вызывается, когда все файлы в задании успешно переданы.<br/> |



 

## <a name="remarks"></a>Remarks

Чтобы получать уведомления, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md) , чтобы указать указатель интерфейса на реализацию **ибаккграундкопикаллбакк** . Чтобы указать, какие уведомления необходимо получать, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md) .

При условии, что указатель интерфейса является допустимым, будут вызываться обратные вызовы. Интерфейс уведомления больше не действителен после завершения работы приложения. Не сохраняет интерфейс уведомления. В результате процесс инициализации приложения должен вызвать метод [**сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md) для тех существующих заданий, для которых вы хотите получить уведомление.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback определен как 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

