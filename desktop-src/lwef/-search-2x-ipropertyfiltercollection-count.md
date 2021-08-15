---
title: Свойство Ипропертифилтерколлектион Count (Вдсшаредидл. h)
description: Число фильтров в коллекции.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- свойство Count устаревшие Windows функции среды
- свойство Count устаревшие Windows функции среды, интерфейс ипропертифилтерколлектион
- интерфейс ипропертифилтерколлектион устаревшие функции среды Windows, свойство Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb24af3aaa73034d2685de35974989bf371aaae79284cbb8120ccffbe41a76cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451074"
---
# <a name="ipropertyfiltercollectioncount-property"></a>Свойство Ипропертифилтерколлектион:: count

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Число фильтров в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на число фильтров в коллекции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





