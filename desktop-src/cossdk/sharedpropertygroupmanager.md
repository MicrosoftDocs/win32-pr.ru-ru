---
description: Создает общие группы свойств и получает доступ к существующим группам общих свойств.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Класс Шаредпропертиграупманажер (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895745"
---
# <a name="sharedpropertygroupmanager-class"></a>Класс Шаредпропертиграупманажер

Создает общие группы свойств и получает доступ к существующим группам общих свойств.

Дополнительные сведения об использовании общих диспетчер свойств в COM+ см. в разделе [com+ shared Диспетчер свойств](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|--------------------------------------------------------------------|
| CLSID      | \_ШАРЕДПРОПЕРТИГРАУПМАНАЖЕР CLSID                                  |
| ProgID:     | L "Мтксспм. Шаредпропертиграупманажер"                               |
| Интерфейсы | [**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Назначение

Используйте этот класс для доступа к методам [**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

## <a name="remarks"></a>Комментарии

Чтобы создать этот объект, вызовите метод [**иобжектконтекст:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Шаредпропертиграупманажер можно объявить с помощью "Комсвкслиб. Шаредпропертиграупманажер" в качестве имени класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**шаредпроперти**](sharedproperty.md)
</dt> <dt>

[**шаредпропертиграуп**](sharedpropertygroup.md)
</dt> </dl>

 

 




