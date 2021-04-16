---
description: Высота элемента в пикселях. Только для чтения.
ms.assetid: 0df73d33-c1ae-43e1-b906-00540e04dfd9
title: Свойство Item. Height
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Height
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 16b4b4a259bf4e1c77fde592c5668f8584b28ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692526"
---
# <a name="itemheight-property"></a>Свойство Item. Height

Высота элемента в пикселях. Только для чтения.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Item.Height
```



## <a name="property-value"></a>Значение свойства

Переменная, которая получает высоту.

## <a name="remarks"></a>Комментарии

Если элемент является цифровой камерой, свойство **Height** представляет высоту изображений, создаваемых этой камерой. Если элемент является сканером, это свойство представляет высоту испытательной информации. Если элемент является изображением, это свойство представляет фактическую высоту изображения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




