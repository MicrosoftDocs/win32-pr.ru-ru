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
ms.openlocfilehash: 136bc160ea81367f8f55ad81cfc06f5e2e272cafae9d7b8f444a65d34e85d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328374"
---
# <a name="featureinfo-object"></a>Объект Феатуреинфо

Объект **феатуреинфо** содержит сведения о целевом компоненте и создается из объекта [**Session**](session-object.md) с помощью метода [**феатуреинфо**](session-featureinfo.md) .

## <a name="members"></a>Элементы

Объект **феатуреинфо** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Объект **феатуреинфо** имеет следующие свойства.



| Свойство.                                                  | Тип доступа           | Описание                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Атрибуты**](featureinfo-attributes.md)<br/>   | Чтение/запись<br/> | Возвращает значение для функции в столбце Attributes таблицы Feature.<br/> |
| [**Описание**](featureinfo-description.md)<br/> |                       | Возвращает описание компонента.<br/>                                          |
| [**Название**](featureinfo-title.md)<br/>             | Только для чтения<br/>  | Возвращает название компонента.<br/>                                                |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ифеатуреинфо определяется как 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Windows Примеры сценариев для установщика](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




