---
title: IDWriteTextFormat2 СетлинеспаЦинг, метод
description: Задать Междустрочный зазор. | IDWriteTextFormat2 СетлинеспаЦинг, метод
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Непосредственная запись метода СетлинеспаЦинг
- Прямая запись метода СетлинеспаЦинг, интерфейс IDWriteTextFormat2
- Прямая запись интерфейса IDWriteTextFormat2, метод СетлинеспаЦинг
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273630"
---
# <a name="idwritetextformat2setlinespacing-method"></a>Метод IDWriteTextFormat2:: СетлинеспаЦинг

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

Тип: **const [**дврите \_ \_ Междустрочный зазор**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***

Управление пространством между строками.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

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

[**IDWriteTextFormat2**](idwritetextformat2.md)
</dt> </dl>

 

 





