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
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415797"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





