---
description: Объект Феатуреинфо содержит сведения о целевом компоненте и создается из объекта Session с помощью метода Феатуреинфо.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Объект Феатуреинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665090"
---
# <a name="featureinfo-object"></a>Объект Феатуреинфо

Объект **феатуреинфо** содержит сведения о целевом компоненте и создается из объекта [**Session**](session-object.md) с помощью метода [**феатуреинфо**](session-featureinfo.md) .

## <a name="members"></a>Элементы

Объект **феатуреинфо** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **феатуреинфо** имеет следующие свойства.



| Свойство                                                  | Тип доступа           | Описание                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Атрибуты**](featureinfo-attributes.md)<br/>   | Чтение/запись<br/> | Возвращает значение для функции в столбце Attributes таблицы Feature.<br/> |
| [**Описание**](featureinfo-description.md)<br/> |                       | Возвращает описание компонента.<br/>                                          |
| [**Заголовок**](featureinfo-title.md)<br/>             | Только для чтения<br/>  | Возвращает название компонента.<br/>                                                |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ифеатуреинфо определяется как 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Примеры сценариев установщик Windows](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




