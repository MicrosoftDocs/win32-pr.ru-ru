---
description: Примечание. Этот интерфейс не рекомендуется к использованию.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Метод Иамфилтердата:: Креатефилтердата ( \_ данные о данных. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675300"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>Метод Иамфилтердата:: Креатефилтердата

> [!Note]  
> Этот интерфейс не рекомендуется к использованию. Новые приложения не должны использовать его.

 

`CreateFilterData`Метод создает двоичные данные реестра для фильтра. Эти данные можно записать в реестр в виде \_ двоичного подраздела reg с именем FilterData в ключе CLSID фильтра.

Как правило, нет причин вызывать этот метод в приложении. Метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) автоматически создает двоичные данные и добавляет их в правильное расположение в реестре. Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*prf2* \[ окне\]
</dt> <dd>

Указатель на структуру [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , содержащую сведения о фильтре.

</dd> <dt>

*пргбфилтердата* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает указатель на двоичные данные. Метод выделяет память для данных. Вызывающий объект должен освободить память, вызвав метод **CoTaskMemFree** .

</dd> <dt>

*ПКБ* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает размер двоичных данных в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В противном случае функция возвращает код ошибки.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Заголовок Headers \_ Data. h находится в каталоге с [образцом модуля сопоставления](mapper-sample.md) в Windows SDK.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>\_Данные о данных. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамфилтердата**](iamfilterdata.md)
</dt> </dl>

 

 




