---
description: Управляет метриками для управляемых элементов.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Класс CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5fd976abf5bce91ffbc5581e73f93c2a8422fcdcbe69fd70745511362e504d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694944"
---
# <a name="cim_metricservice-class"></a>\_Класс CIM метриксервице

Управляет метриками для управляемых элементов.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **CIM \_ метриксервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **CIM \_ метриксервице** содержит следующие методы.



| Метод                                                                   | Описание                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**контролметрикс**](cim-metricservice-controlmetrics.md)               | Включает и отключает сбор метрик.<br/>                                                                                                                          |
| [**контролметриксбикласс**](cim-metricservice-controlmetricsbyclass.md) | Включает и отключает сбор метрик для класса.<br/>                                                                                                              |
| [**контролсамплетимес**](cim-metricservice-controlsampletimes.md)       | Указывает, когда собираются метрики.<br/>                                                                                                                                     |
| [**жетметриквалуес**](cim-metricservice-getmetricvalues.md)             | Извлекает отфильтрованный список значений метрик.<br/>                                                                                                                              |
| [**шовметрикс**](cim-metricservice-showmetrics.md)                     | Указывает, включена ли коллекция метрик для указанных управляемых элементов, и указывает метрики, доступные для коллекции для каждого управляемого элемента.<br/> |
| [**шовметриксбикласс**](cim-metricservice-showmetricsbyclass.md)       | Указывает, какие метрики доступны для коллекции для всех экземпляров класса CIM.<br/>                                                                                   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




