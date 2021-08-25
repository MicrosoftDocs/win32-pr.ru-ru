---
title: Интерфейс INapComponentConfig3 (Напкоммон. h)
description: Предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV) для установки и изменения данных конфигурации для конкретного идентификатора конфигурации.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 интерфейса NAP
- INapComponentConfig3 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea8ab7b42589fa548439b03c04ade56db498750ccd47841b806dcb6b506d3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803084"
---
# <a name="inapcomponentconfig3-interface"></a>Интерфейс INapComponentConfig3

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Интерфейс **INapComponentConfig3** предоставляет методы настройки системы защиты доступа к сети для средств проверки работоспособности системы (SHV) для установки и изменения данных конфигурации для конкретного идентификатора конфигурации.

> [!Note]  
> Этот интерфейс наследует все методы [**INapComponentConfig2**](inapcomponentconfig2.md) и использовать вместо него.

 

## <a name="members"></a>Элементы

Интерфейс **INapComponentConfig3** наследует от [**INapComponentConfig2**](inapcomponentconfig2.md). **INapComponentConfig3** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **INapComponentConfig3** содержит следующие методы.



| Метод                                                                                | Описание                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D Елетеаллконфиг**](inapcomponentconfig3-deleteallconfig.md) | Реализуется средствами SHV для предоставления способа сброса хранилища SHV в исходное состояние после установки.<br/>      |
| [**INapComponentConfig3::D Елетеконфиг**](inapcomponentconfig3-deleteconfig.md)       | Реализуется средствами SHV для предоставления способа удаления данных конфигурации для определенного идентификатора конфигурации.<br/>  |
| [**INapComponentConfig3:: Жетконфигфромид**](inapcomponentconfig3-getconfigfromid.md) | Реализуется средствами SHV, чтобы предоставить способ получения данных конфигурации для определенного идентификатора конфигурации.<br/>  |
| [**INapComponentConfig3:: документе newconfig**](inapcomponentconfig3-newconfig.md)             | Реализуется средствами SHV, чтобы предоставить способ создания данных конфигурации для определенного идентификатора конфигурации.<br/>  |
| [**INapComponentConfig3:: Сетконфигтоид**](inapcomponentconfig3-setconfigtoid.md)     | Реализуется средствами SHV для предоставления способа установки данных конфигурации для конкретного идентификатора конфигурации.<br/> |



 

## <a name="remarks"></a>Remarks

Этот интерфейс не должен реализовываться агентами работоспособности системы (SHA) или клиентами принудительного применения карантина (кекс).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Напкоммон. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Напкоммон. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[Интерфейсы NAP](nap-interfaces.md)
</dt> <dt>

[Справочник по NAP](nap-reference.md)
</dt> </dl>

 

 





