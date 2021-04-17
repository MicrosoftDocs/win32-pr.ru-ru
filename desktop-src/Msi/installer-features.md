---
description: Свойство Features является свойством только для чтения, которое возвращает объект Стринглист, перечисляющий набор опубликованных компонентов для указанного продукта.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Свойство Installer. Features
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651620"
---
# <a name="installerfeatures-property"></a>Свойство Installer. Features

Свойство **Features** является свойством только для чтения, которое возвращает объект [**стринглист**](stringlist-object.md) , перечисляющий набор опубликованных компонентов для указанного продукта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Значение свойства

Указывает код продукта.

## <a name="remarks"></a>Комментарии

Чтобы перечислить функции, приложение выполняет перебор объекта [**стринглист**](stringlist-object.md) , используя для каждой конструкции. Поскольку функции не упорядочены, каждая новая функция имеет произвольный индекс, то есть функция может возвращать функции в любом порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумфеатурес**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Функции состояния системы](installer-function-reference.md)
</dt> </dl>

 

 




