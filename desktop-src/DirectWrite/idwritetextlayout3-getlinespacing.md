---
title: IDWriteTextLayout3 ЖетлинеспаЦинг, метод
description: Возвращает сведения о межстрочном промежутке.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Непосредственная запись метода ЖетлинеспаЦинг
- Прямая запись метода ЖетлинеспаЦинг, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод ЖетлинеспаЦинг
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988889"
---
# <a name="idwritetextlayout3getlinespacing-method"></a>Метод IDWriteTextLayout3:: ЖетлинеспаЦинг

Возвращает сведения о межстрочном промежутке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*линеспаЦингоптионс* \[ заполняет\]
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

 

 





