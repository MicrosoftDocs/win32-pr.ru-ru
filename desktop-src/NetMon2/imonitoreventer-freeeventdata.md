---
description: Метод Фриевентдата освобождает место, выделенное для структуры НМЕВЕНТДАТА.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Метод Имониторевентер:: Фриевентдата (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673179"
---
# <a name="imonitoreventerfreeeventdata-method"></a>Метод Имониторевентер:: Фриевентдата

Метод **фриевентдата** освобождает место, выделенное для структуры [**нмевентдата**](nmeventdata.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнмевентдата* \[ окне\]
</dt> <dd>

Адрес структуры [**нмевентдата**](nmeventdata.md) , памяти, из которой освобождается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Мониторы вызывают этот метод, чтобы освободить память, выделенную для структуры данных события. Имейте в виду, что хотя у монитора по-прежнему есть указатель на строки в выделенной структуре [**нмевентдата**](nmeventdata.md) , память для этих строк должна быть освобождена до вызова метода **фриевентдата** .

Дополнительные сведения о том, как выделить память для структуры [**нмевентдата**](nmeventdata.md) , см. в разделе [**Имониторевентер:: жетевентдата**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имониторевентер**](imonitoreventer.md)
</dt> <dt>

[**Имониторевентер:: Жетевентдата**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**нмевентдата**](nmeventdata.md)
</dt> </dl>

 

 




