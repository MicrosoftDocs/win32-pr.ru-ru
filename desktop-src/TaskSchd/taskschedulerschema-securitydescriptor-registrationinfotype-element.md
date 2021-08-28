---
title: SecurityDescriptor (Регистратионинфотипе), элемент
description: Указывает дескриптор безопасности задачи.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- планировщик задач элемента SecurityDescriptor
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83742ebbbc6b8fb653610bf8e20c00094a3c8a3984123765adf6e953935c9011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099864"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>SecurityDescriptor (Регистратионинфотипе), элемент

Указывает дескриптор безопасности задачи.

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

Элемент **SecurityDescriptor** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                           | Унаследован от                                                                         | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев дескриптор безопасности задачи указывается с помощью свойства [**регистратионинфо. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .

Для разработки на C++ дескриптор безопасности задачи указывается с помощью свойства [**ирегистратионинфо:: SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





