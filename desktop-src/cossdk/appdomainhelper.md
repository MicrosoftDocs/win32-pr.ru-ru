---
description: Привязывает управляемый объект к домену приложения, который является изолированной средой, в которой выполняются приложения.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Класс Аппдомаинхелпер (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: bab1ade7d97d3e911dbe0dc56cff69c5308d7d5e44baadb4641829c5f5a9d806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917558"
---
# <a name="appdomainhelper-class"></a>Класс Аппдомаинхелпер

Привязывает управляемый объект к домену приложения, который является изолированной средой, в которой выполняются приложения.

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ аппдомаинхелпер                                 |
| ProgID:     | L "System. EnterpriseServices. internal. Аппдомаинхелпер" |
| Интерфейсы | [**иаппдомаинхелпер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a>Назначение

Используйте этот класс для доступа к методам [**иаппдомаинхелпер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).

## <a name="remarks"></a>Remarks

Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

чтобы использовать этот класс из Visual Basic майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Аппдомаинхелпер можно объявить с помощью "Комсвкслиб. Аппдомаинхелпер" в качестве имени класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иаппдомаинхелпер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

