---
title: Метод IDWriteTextLayout2ических метрик
description: Получает общие метрики для форматированной строки.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Прямая запись методаических метрик
- Интерфейс IDWriteTextLayout2 с прямым написанием с методомических метрик
- Интерфейс IDWriteTextLayout2 Direct Write, методических метрик
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681952"
---
# <a name="idwritetextlayout2getmetrics-method"></a>Метод IDWriteTextLayout2:: с метриками

Получает общие метрики для форматированной строки.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

 *текстметрикс* \[ заполняет\]
</dt> <dd>

Введите: **[**дврите \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _

При возврате из этого метода содержит измеряемое расстояние текста и связанного содержимого после форматирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





