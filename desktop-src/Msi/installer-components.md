---
description: Свойство "компоненты только для чтения" возвращает объект Стринглист, перечисляющий набор установленных компонентов для всех продуктов.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Свойство Installer. Components
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652074"
---
# <a name="installercomponents-property"></a>Свойство Installer. Components

Свойство " **компоненты** только для чтения" возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор установленных компонентов для всех продуктов.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Чтобы перечислить компоненты, приложение может выполнить итерацию по объекту [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Поскольку компоненты не упорядочены, все новые компоненты имеют произвольный индекс. Это означает, что функция может возвращать компоненты в любом порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумкомпонентс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




