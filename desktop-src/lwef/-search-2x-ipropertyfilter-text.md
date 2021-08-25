---
title: Свойство Text Ипропертифилтер (Вдсшаредидл. h)
description: Текст фильтра.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- свойства текста устаревшие Windows функции среды
- свойства текста устаревшие Windows функции среды, интерфейс ипропертифилтер
- интерфейс ипропертифилтер устаревшие функции среды Windows, свойство Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5dd572fe2edf82b2e882b73e2aec772090afda791117b0c1ac2fb14b115f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963804"
---
# <a name="ipropertyfiltertext-property"></a>Свойство Ипропертифилтер:: Text

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Текст фильтра.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a>Значение свойства

Задает текст фильтра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Заголовок<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





