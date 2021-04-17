---
description: Метод Fetch объекта View возвращает следующую строку данных столбца, если в результирующем наборе доступно больше строк, в противном случае — значение null. Вызовите метод Execute перед методом FETCH.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: Метод представления. FETCH
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674887"
---
# <a name="viewfetch-method"></a>Метод представления. FETCH

Метод **Fetch** объекта [**View**](view-object.md) возвращает следующую строку данных столбца, если в результирующем наборе доступно больше строк, в противном случае — значение null. Вызовите метод [**EXECUTE**](view-execute.md) перед методом **Fetch** .

## <a name="syntax"></a>Синтаксис


```JScript
View.Fetch()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Один и тот же объект [**записи**](record-object.md) следует использовать для получения данных в нескольких строках, иначе объект должен быть освобожден путем выхода из области видимости. Запись можно проверить на конец результирующего набора, используя синтаксис "If Фетчрекорд Nothing".

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView определен как 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




