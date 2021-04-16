---
description: Свойство SourcePath объекта Session является свойством, предназначенным только для чтения и предоставляющим полный путь к указанной папке на исходном носителе или образе сервера.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Свойство Session. SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679939"
---
# <a name="sessionsourcepath-property"></a>Свойство Session. SourcePath

Свойство **SourcePath** объекта [**Session**](session-object.md) является свойством, предназначенным только для чтения и предоставляющим полный путь к указанной папке на исходном носителе или образе сервера.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Значение свойства

Обязательное с учетом регистра имя свойства папки, заданное первичным ключом [таблицы Directory](directory-table.md). Если папка не существует, возникает ошибка.

## <a name="remarks"></a>Комментарии

Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




