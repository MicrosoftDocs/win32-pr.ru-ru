---
title: URI (Регистратионинфотипе), элемент
description: Указывает универсальный код ресурса (URI) задачи.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- планировщик задач элемента URI
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b9a2d9b8faf327f7b64be2cdd4273f2252405767004dc6e0d58b0c95b5f1910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355607"
---
# <a name="uri-registrationinfotype-element"></a>URI (Регистратионинфотипе), элемент

Указывает универсальный код ресурса (URI) задачи. Этот элемент используется для указания места размещения зарегистрированной задачи в иерархии папок задач.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

Элемент **URI** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                           | Унаследован от                                                                         | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев URI задачи указывается с помощью свойства [**регистратионинфо. URI**](registrationinfo-uri.md) .

Для разработки на C++ URI задачи указывается с помощью свойства [**ирегистратионинфо:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





