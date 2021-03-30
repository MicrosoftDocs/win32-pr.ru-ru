---
title: Тасксеттингс. Нетворксеттингс, свойство
description: Для создания скриптов Возвращает или задает объект параметров сети, который содержит идентификатор и имя сетевого профиля.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- планировщик задач свойства Нетворксеттингс
- Планировщик задач свойства Нетворксеттингс, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Нетворксеттингс
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801469"
---
# <a name="tasksettingsnetworksettings-property"></a>Тасксеттингс. Нетворксеттингс, свойство

Для создания скриптов Возвращает или задает объект параметров сети, который содержит идентификатор и имя сетевого профиля. Если свойство [**рунонлифнетворкаваилабле**](tasksettings-runonlyifnetworkavailable.md) объекта [**Тасксеттингс**](tasksettings.md) имеет **значение true** и в свойстве **нетворксеттингс** указан сетевой пропфиле, задача будет запущена только в том случае, если доступен указанный сетевой профиль.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Значение свойства

Объект [**нетворксеттингс**](networksettings.md) , содержащий идентификатор и имя сетевого профиля.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**тасксеттингс**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





