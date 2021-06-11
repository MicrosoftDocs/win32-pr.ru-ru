---
description: Узнайте о методе Иамфилтердата::P Арсефилтердата, который распаковать двоичные данные реестра для фильтра. Этот интерфейс не рекомендуется к использованию.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Иамфилтердата::P метод Арсефилтердата ( \_ данные о данных. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989449"
---
# <a name="iamfilterdataparsefilterdata-method"></a>Иамфилтердата: метод:P Арсефилтердата

> [!Note]  
> Этот интерфейс не рекомендуется к использованию. Новые приложения не должны использовать его.

 

`ParseFilterData`Метод распаковать двоичные данные реестра для фильтра.

Как правило, нет причин вызывать этот метод в приложении. Метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) предоставляет более удобный способ доступа к данным в реестре фильтров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ргбфилтердата* \[ окне\]
</dt> <dd>

Указатель на двоичные данные реестра. Эти данные можно получить, извлекая свойство "FilterData" из моникера фильтра. Данные хранятся в виде массива **SAFEARRAY** в байтах (VT \_ UI1 \| VT \_ ).

</dd> <dt>

*CB* \[ окне\]
</dt> <dd>

Задает размер двоичных данных в байтах.

</dd> <dt>

*prgbRegFilter2* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает указатель на распакованные данные. При возврате из метода приведите этот указатель к типу [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , чтобы получить доступ к данным фильтра. Вызывающий объект должен освободить память, вызвав метод **CoTaskMemFree** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В противном случае функция возвращает код ошибки.

## <a name="remarks"></a>Remarks

> [!Note]  
> Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>\_Данные о данных. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамфилтердата**](iamfilterdata.md)
</dt> </dl>

 

 




