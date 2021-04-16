---
description: Свойство TargetPath объекта Session — это свойство, доступное для чтения и записи, которое предоставляет полный путь к указанной папке на целевом диске установки.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Свойство Session. TargetPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652243"
---
# <a name="sessiontargetpath-property"></a>Свойство Session. TargetPath

Свойство **TargetPath** объекта [**Session**](session-object.md) — это свойство, доступное для чтения и записи, которое предоставляет полный путь к указанной папке на целевом диске установки.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Значение свойства

Обязательное с учетом регистра имя свойства папки, заданное первичным ключом [таблицы Directory](directory-table.md). Если папка не существует, возникает ошибка.

## <a name="remarks"></a>Комментарии

Не пытайтесь настроить целевой путь, если компоненты, использующие эти пути, уже установлены для текущего пользователя или для другого пользователя. Проверьте свойство [**продуктстате**](productstate.md) , чтобы определить, установлен ли продукт, содержащий компонент.

Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




