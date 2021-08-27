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
ms.openlocfilehash: ac05dcc813192a9ea1bf1f1f4e5ad63ed72eca6874de855ac3f4582af51680f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120364"
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

## <a name="remarks"></a>Remarks

Чтобы создать этот объект, вызовите метод [**иобжектконтекст:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

чтобы использовать этот класс из Visual Basic майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Шаредпропертиграупманажер можно объявить с помощью "Комсвкслиб. Шаредпропертиграупманажер" в качестве имени класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ишаредпропертиграупманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**шаредпроперти**](sharedproperty.md)
</dt> <dt>

[**шаредпропертиграуп**](sharedpropertygroup.md)
</dt> </dl>

 

 




