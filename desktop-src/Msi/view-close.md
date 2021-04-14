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
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675642"
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

## <a name="remarks"></a>Комментарии

Этот метод должен вызываться перед повторным вызовом метода [**EXECUTE**](view-execute.md) для объекта [**View**](view-object.md) , если только не были получены все строки результирующего набора с помощью метода [**Fetch**](view-fetch.md) . Он вызывается внутренним образом при уничтожении представления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView определен как 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




