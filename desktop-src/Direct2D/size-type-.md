---
title: Функция типа size (D2d1helper. h)
description: Создает структуру размера, в которой хранятся значения ширины и высоты, используя указанный тип данных.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Тип размера функция Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490149"
---
# <a name="sizetype-function"></a>Size, <Type> функция

Создает структуру размера, в которой хранятся значения ширины и высоты, используя указанный тип данных.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Параметры шаблона



| Параметр | Описание                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Тип      | Тип данных, используемый для хранения ширины и высоты размера. Возможными значениями являются FLOAT и UINT32. |



 

## <a name="parameters"></a>Параметры



| Параметр | Описание        |
|-----------|--------------------|
| width     | Ширина размера.  |
| рост    | Высота размера. |



 

## <a name="return-value"></a>Возвращаемое значение

Размер, который содержит указанные ширину и высоту.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Библиотека<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





