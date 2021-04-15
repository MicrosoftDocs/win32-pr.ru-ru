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
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675747"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ исуммаринфо определяется как 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




