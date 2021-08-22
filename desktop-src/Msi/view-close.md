---
description: Метод Close объекта View прерывает выполнение запроса и освобождает ресурсы базы данных.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: Метод View. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: edbf2dd30902fa437fdd67d21efb86bb2edeabbd499f0f022501f166ad1b92a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498854"
---
# <a name="viewclose-method"></a>Метод View. Close

Метод **Close** объекта [**View**](view-object.md) прерывает выполнение запроса и освобождает ресурсы базы данных.

## <a name="syntax"></a>Синтаксис


```JScript
View.Close()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод должен вызываться перед повторным вызовом метода [**EXECUTE**](view-execute.md) для объекта [**View**](view-object.md) , если только не были получены все строки результирующего набора с помощью метода [**Fetch**](view-fetch.md) . Он вызывается внутренним образом при уничтожении представления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView определен как 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




