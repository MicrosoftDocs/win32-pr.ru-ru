---
description: Свойство Компоненткуалифиерс является свойством только для чтения, которое возвращает объект Стринглист, перечисляющий набор зарегистрированных квалификаторов для указанного компонента.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Свойство Installer. Компоненткуалифиерс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651964"
---
# <a name="installercomponentqualifiers-property"></a>Свойство Installer. Компоненткуалифиерс

Свойство **компоненткуалифиерс** является свойством только для чтения, которое возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор зарегистрированных квалификаторов для указанного компонента.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Значение свойства

Строковый идентификатор GUID, представляющий категорию [компонента](publishcomponent-table.md).

## <a name="remarks"></a>Комментарии

Чтобы перечислить квалификаторы, приложение выполняет итерацию объекта [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Поскольку квалификаторы не упорядочены, каждый новый квалификатор имеет произвольный индекс, то есть функция может возвращать квалификаторы в любом порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




