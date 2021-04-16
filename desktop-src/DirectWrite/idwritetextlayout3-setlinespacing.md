---
title: IDWriteTextLayout3 СетлинеспаЦинг, метод
description: Задать Междустрочный зазор. | IDWriteTextLayout3 СетлинеспаЦинг, метод
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Непосредственная запись метода СетлинеспаЦинг
- Прямая запись метода СетлинеспаЦинг, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод СетлинеспаЦинг
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664858"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>Метод IDWriteTextLayout3:: СетлинеспаЦинг

Задать Междустрочный зазор.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*линеспаЦингоптионс* \[ окне\]
</dt> <dd>

Управление пространством между строками.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                 |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





