---
title: Функция типа Point2 (D2d1helper. h)
description: Создает точку, в которой хранятся координаты, используя указанный тип данных.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Функция типа Point2 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654558"
---
# <a name="point2type-function"></a><Type>Функция Point2

Создает точку, в которой хранятся координаты, используя указанный тип данных.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Параметры шаблона



| Параметр | Описание                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| Тип      | Тип данных, используемый для хранения координаты x и координаты y точки. Возможными значениями являются FLOAT и UINT32. |



 

## <a name="parameters"></a>Параметры



| Параметр | Описание                    |
|-----------|--------------------------------|
| x         | Координата X точки. |
| да         | Координата Y точки. |



 

## <a name="return-value"></a>Возвращаемое значение

Точка, которая содержит заданную координату x и y.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Библиотека<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





