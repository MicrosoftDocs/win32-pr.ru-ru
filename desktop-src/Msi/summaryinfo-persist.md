---
description: Метод PERSISTED объекта Суммаринфо форматирует и записывает ранее сохраненные свойства в стандартный поток SummaryInformation.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: Суммаринфо. PERSISTED, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 35916dccc3b131d49176b4ecc1a31fedf40c7c5eafeb4c107b30de08db21dc81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039604"
---
# <a name="summaryinfopersist-method"></a>Суммаринфо. PERSISTED, метод

Метод **PERSISTED** объекта [**суммаринфо**](summaryinfo-object.md) форматирует и записывает ранее сохраненные свойства в стандартный поток SummaryInformation. Он выдает ошибку, если поток не может быть успешно записан. Этот метод может вызываться только один раз после задания всех значений свойств. Свойства по-прежнему могут быть считаны после того, как поток записывается.

## <a name="syntax"></a>Синтаксис


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ исуммаринфо определяется как 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




