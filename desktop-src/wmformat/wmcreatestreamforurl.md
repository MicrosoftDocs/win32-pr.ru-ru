---
title: Функция Вмкреатестреамфорурл
description: Функция Вмкреатестреамфорурл реализуется приложением для создания объекта COM IStream для данного URL-адреса.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Вмкреатестреамфорурл функция Windows Media Format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c32302147eeb814c211a77555ab1c9bb3614eddf3d8001015479461e05d40ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653457"
---
# <a name="wmcreatestreamforurl-function"></a>Функция Вмкреатестреамфорурл

Функция **вмкреатестреамфорурл** реализуется приложением для создания объекта COM **IStream** для данного URL-адреса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзурл* \[ окне\]
</dt> <dd>

Указатель на строку расширенных символов, содержащую URL-адрес.

</dd> <dt>

*пфкорректсаурце* \[ заполняет\]
</dt> <dd>

Указатель на флаг, true запрещает пакету SDK пытаться выполнять другие подключаемые модули источника для этого URL-адреса.

</dd> <dt>

*ппстреам* \[ заполняет\]
</dt> <dd>

Указатель на указатель на объект **IStream** , созданный методом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, она должна вернуть значение S \_ ОК. В случае сбоя он должен вернуть соответствующий код ошибки **HRESULT** , а \* *Ппстреам* должен иметь значение **null**.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подключаемые модули источника**](source-plug-ins.md)
</dt> </dl>

 

 




