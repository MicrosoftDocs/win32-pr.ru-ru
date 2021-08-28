---
description: Представляет службу, которая может создавать, применять и удалять моментальные снимки виртуальных систем.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: Класс CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5546c7381eb0830d820af20d7efa03e5d7441a712b872a3ae2167b3e441354d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682694"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a>\_Класс CIM виртуалсистемснапшотсервице

Представляет службу, которая может создавать, применять и удалять моментальные снимки виртуальных систем.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалсистемснапшотсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **CIM \_ виртуалсистемснапшотсервице** содержит следующие методы.



| Метод                                                                      | Описание                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**апплиснапшот**](cim-virtualsystemsnapshotservice-applysnapshot.md)     | Применяет моментальный снимок виртуальной системы к виртуальной системе в исходной виртуальной системе.<br/> |
| [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)   | Создает моментальный снимок виртуальной системы.<br/>                                               |
| [**дестройснапшот**](cim-virtualsystemsnapshotservice-destroysnapshot.md) | Удаляет моментальный снимок виртуальной системы.<br/>                                                    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




