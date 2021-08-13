---
title: IDWriteFont2 Исколорфонт, метод
description: Позволяет определить, является ли путь визуализации цвета потенциально необходимым.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Непосредственная запись метода Исколорфонт
- Прямая запись метода Исколорфонт, интерфейс IDWriteFont2
- Прямая запись интерфейса IDWriteFont2, метод Исколорфонт
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 144aded290c7a4121dd785a1844971e3c1b5501b8ae78707d8da5378c44b002a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650188"
---
# <a name="idwritefont2iscolorfont-method"></a>Метод IDWriteFont2:: Исколорфонт

Позволяет определить, является ли путь визуализации цвета потенциально необходимым.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

Возвращает **значение true** , если шрифт имеет сведения о цвете (таблицы КОЛР и кпал); в противном случае — **false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





