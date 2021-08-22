---
description: Управляет конфигурацией пулов ресурсов с помощью заданий.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Класс CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6a289c21f4a741778bb88a154f5923cf844f0c78390c50b558d40a5bcc32aff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647669"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a>\_Класс CIM ресаурцепулконфигуратионсервице

Управляет конфигурацией пулов ресурсов с помощью заданий.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ресаурцепулконфигуратионсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **CIM \_ ресаурцепулконфигуратионсервице** содержит следующие методы.



| Метод                                                                                                          | Описание                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**аддресаурцесторесаурцепул**](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | Запускает задание по добавлению ресурсов в пул ресурсов.<br/>                  |
| [**чанжепарентресаурцепул**](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | Запустите задание, чтобы изменить родительский пул ресурсов пула ресурсов.<br/> |
| [**креатечилдресаурцепул**](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | Запустите задание, чтобы создать пул ресурсов из родительского пула ресурсов.<br/> |
| [**CreateResourcePool**](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | Запускает задание для создания пула корневых ресурсов.<br/>                       |
| [**делетересаурцепул**](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | Запуск задания для удаления пула ресурсов.<br/>                             |
| [**ремовересаурцесфромресаурцепул**](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | Запускает задание по удалению ресурсов из пула ресурсов.<br/>             |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




