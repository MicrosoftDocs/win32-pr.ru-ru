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
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538735"
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

## <a name="remarks"></a>Комментарии

Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+. Объект Аппдомаинхелпер можно объявить с помощью "Комсвкслиб. Аппдомаинхелпер" в качестве имени класса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Комсвкс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иаппдомаинхелпер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

