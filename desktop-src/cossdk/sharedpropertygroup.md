---
description: Создает и обращается к общим свойствам в группе общих свойств.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Класс Шаредпропертиграуп (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807277"
---
# <a name="sharedpropertygroup-class"></a>Класс Шаредпропертиграуп

Создает и обращается к общим свойствам в группе общих свойств.

Дополнительные сведения об использовании общих диспетчер свойств в COM+ см. в разделе [com+ shared Диспетчер свойств](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|------------------------------------------------------|
| Интерфейсы | [**ишаредпропертиграуп**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a>Назначение

Используйте этот класс для доступа к методам [**ишаредпропертиграуп**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).

## <a name="remarks"></a>Комментарии

Объект **шаредпропертиграуп** можно создать с помощью метода [**креатепропертиграуп**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) объекта [**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Шаредпропертиграуп создается путем вызова метода [**креатепропертиграуп**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) объекта [**шаредпропертиграупманажер**](sharedpropertygroupmanager.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ишаредпропертиграуп**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[**шаредпроперти**](sharedproperty.md)
</dt> <dt>

[**шаредпропертиграупманажер**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




