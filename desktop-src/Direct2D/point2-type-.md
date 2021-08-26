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
ms.openlocfilehash: e79208c0e68736ae91d623622c13bbeb624ab760
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887199"
---
# <a name="point2lttypegt-function"></a>&lt;Функция типа &gt; Point2

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
| y         | Координата Y точки. |



 

## <a name="return-value"></a>Возвращаемое значение

Точка, которая содержит заданную координату x и y.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для приложений для \[ классических приложений Windows Vista \|\]<br/>                          |
| Минимальная версия сервера<br/> | Windows сервер 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008 приложения \[ UWP для классических приложений \|\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Заголовок<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Библиотека<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





