---
title: Свойство Нестингдепс Ипропертифилтер (Вдсшаредидл. h)
description: Отфильтровывает глубину внутри вложенного набора круглых скобок.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Свойства Нестингдепс устаревшие функции среды Windows
- Свойства Нестингдепс устаревшие функции среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство Нестингдепс
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
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415480"
---
# <a name="ipropertyfilternestingdepth-property"></a>Свойство Ипропертифилтер:: Нестингдепс

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

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
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





