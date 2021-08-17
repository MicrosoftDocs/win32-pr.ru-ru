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
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059661"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**тасксеттингс**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





