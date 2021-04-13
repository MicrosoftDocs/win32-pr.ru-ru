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
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342772"
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



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ гуестсервице**](msvm-guestservice.md)
</dt> </dl>

 

 




