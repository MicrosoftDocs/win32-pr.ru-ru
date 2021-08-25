---
title: Свойство UID Ипропертифилтер (Вдсшаредидл. h)
description: Идентификатор UID для свойства, по которому производится фильтрация.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- свойства UID, устаревшие Windows функции среды
- свойства UID, устаревшие Windows функции среды, интерфейс ипропертифилтер
- интерфейс ипропертифилтер устаревшие функции среды Windows, свойство UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0e96fc2c207a3dc7e11d751cb2e545f6d917036b3ce8f184280807c71f55e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963784"
---
# <a name="ipropertyfilteruid-property"></a>Свойство Ипропертифилтер:: UID

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Идентификатор UID для свойства, по которому производится фильтрация.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Значение свойства

Задает свойство UID.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Заголовок<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





