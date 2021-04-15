---
description: Объект Компонентинфо представляет дополнительные сведения о компоненте, который можно получить с помощью вызова из Мсижеткомпонентпасекс.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Объект Компонентинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651885"
---
# <a name="componentinfo-object"></a>Объект Компонентинфо

Объект Компонентинфо представляет дополнительные сведения о компоненте, который можно получить с помощью вызова из Мсижеткомпонентпасекс.

**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается. Этот объект доступен, начиная с установщик Windows 5,0.

## <a name="members"></a>Элементы

Объект **компонентинфо** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **компонентинфо** имеет следующие свойства.



| Свойство                                                        | Описание                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**компоненткоде**](componentinfo-componentcode.md)<br/> | Код компонента рассматриваемого компонента.<br/> |
| [**Путь**](componentinfo-componentcode.md)<br/>          | Путь к компоненту.<br/>                       |
| [**Состояние**](componentinfo-state.md)<br/>                 | Состояние компонента.<br/>                      |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 или более поздней версии.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ икомпонентинфо определен как 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование интерфейса автоматизации](using-the-automation-interface.md)
</dt> <dt>

[Примеры сценариев установщик Windows](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




