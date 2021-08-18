---
title: Свойство Нестингдепс Ипропертифилтер (Вдсшаредидл. h)
description: Отфильтровывает глубину внутри вложенного набора круглых скобок.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- свойства нестингдепс устаревшей среды Windows
- свойства нестингдепс устаревшей среды Windows, интерфейс ипропертифилтер
- интерфейс ипропертифилтер устаревшие функции среды Windows, свойство нестингдепс
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2499d7a3d5505f4cb428cbc8831ec0ea4e0a71843693f5a8ba1250995071df32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481212"
---
# <a name="ipropertyfilternestingdepth-property"></a>Свойство Ипропертифилтер:: Нестингдепс

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Отфильтровывает глубину внутри вложенного набора круглых скобок.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a>Значение свойства

Задает число, указывающее глубину вложенных круглых скобок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





