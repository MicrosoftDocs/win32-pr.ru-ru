---
description: Метод Кскуеримедиумс извлекает средние, поддерживаемые ПИН-кодом.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Метод Икспин:: Кскуеримедиумс (Кспрокси. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 33edb7cb2ca959080878f7ce735930ceec9d95dc2f829aef6d50f72d764f2f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398940"
---
# <a name="ikspinksquerymediums-method"></a>Метод Икспин:: Кскуеримедиумс

`KsQueryMediums`Метод извлекает средние, поддерживаемые ПИН-кодом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппми* \[ заполняет\]
</dt> <dd>

Адрес указателя на структуру [**\_ элемента ксмултипле**](ksmultiple-item.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод возвращает выделенную задачей структуру [**\_ элемента ксмултипле**](ksmultiple-item.md) , за которой следует ноль или более структур [**регпинмедиум**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) . Элемент **Count** в структуре **\_ элемента Ксмултипле** указывает количество структур **регпинмедиум** . Каждая структура **регпинмедиум** определяет средний уровень, поддерживаемый ПИН-кодом.

Вызывающий объект должен освобождать возвращаемые структуры с помощью функции **CoTaskMemFree** .

Перед Кспрокси. h необходимо включить KS. h.

## <a name="examples"></a>Примеры

Следующая вспомогательная функция пытается сопоставить ПИН-код с указанным носителем.


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Кспрокси. h</dt> </dl>    |
| Библиотека<br/>                  | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс Икспин**](ikspin.md)
</dt> <dt>

[Фильтры драйвера класса WDM](wdm-class-driver-filters.md)
</dt> </dl>

 

 




