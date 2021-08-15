---
title: Свойство DisplayName Иресултпроперти (Вдсшаредидл. h)
description: Локализованное отображаемое имя свойства.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- функции свойства DisplayName прежних версий Windows
- свойства DisplayName прежних версий Windows функции среды, интерфейс иресултпроперти
- интерфейс иресултпроперти устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e15eedcafffbae25b2671b02aaac8fd1e64b625edfea3e040ed2c6067ca953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755166"
---
# <a name="iresultpropertydisplayname-property"></a>Иресултпроперти: свойство Исплайнаме:D

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Локализованное отображаемое имя свойства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на локализованное отображаемое имя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





