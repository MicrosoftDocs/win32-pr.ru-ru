---
description: Представляет гостевую службу VSS. Он используется для запроса данных гостевого кластера с узла Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Класс Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c84e9fd96ea4f82c5e89138cfb75f42e2bd184f66926d7139958f485273d6425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014472"
---
# <a name="msvm_vssservice-class"></a>\_Класс мсвм всссервице

Представляет гостевую службу VSS. Он используется для запроса данных гостевого кластера с узла Hyper-V.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ всссервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ всссервице** содержит следующие методы.



| Метод                                                                               | Описание                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**куеригуестклустеринформатион**](msvm-vssservice-queryguestclusterinformation.md) | Запрос сведений о кластере от узла Hyper-V к гостевой системе.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ гуестсервице**](msvm-guestservice.md)
</dt> </dl>

 

 




