---
title: Интерфейс Ибаккграундкопиманажер (Deliveryoptimization. h)
description: Создает задания перемещения, извлекает объект перечислителя, содержащий задания в очереди, и получает отдельные задания из очереди.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Интерфейс Ибаккграундкопиманажер
- Интерфейс Ибаккграундкопиманажер, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988777"
---
# <a name="ibackgroundcopymanager-interface"></a>Интерфейс Ибаккграундкопиманажер

Создает задания перемещения, извлекает объект перечислителя, содержащий задания в очереди, и получает отдельные задания из очереди.

## <a name="members"></a>Элементы

Интерфейс **ибаккграундкопиманажер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ибаккграундкопиманажер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ибаккграундкопиманажер** содержит следующие методы.



| Метод                                                | Описание                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Создает задание перемещения.<br/>                   |
| [**жетжоб**](ibackgroundcopymanager-getjob.md)       | Извлекает указанное задание из очереди.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager определен как 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

