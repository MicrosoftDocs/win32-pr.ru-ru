---
description: Метод Get получает свойство, определяемое идентификатором GUID набора свойств и ИДЕНТИФИКАТОРом свойства.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Метод Икспропертисет:: Get (Кспрокси. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: fbfd44002270209c055b5a4003d9062a6821aeffb3ce71de7977fc20d0c64e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652246"
---
# <a name="ikspropertysetget-method"></a>Метод Икспропертисет:: Get

Метод **Get** получает свойство, ОПРЕДЕЛЯЕМое идентификатором GUID набора свойств и идентификатором свойства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*гуидпропсет* \[ окне\]
</dt> <dd>

Идентификатор GUID набора свойств.

</dd> <dt>

*dwPropID* \[ окне\]
</dt> <dd>

Идентификатор свойства в наборе свойств.

</dd> <dt>

*пинстанцедата* \[ окне\]
</dt> <dd>

Указатель на массив байтов, содержащий данные экземпляра для свойства.

</dd> <dt>

*кбинстанцедата* \[ окне\]
</dt> <dd>

Размер массива, заданного в *пинстанцедата*, в байтах.

</dd> <dt>

*ппропдата* \[ заполняет\]
</dt> <dd>

Указатель на массив байтов, который получает данные свойства.

</dd> <dt>

*кбпропдата* \[ окне\]
</dt> <dd>

Размер массива, заданного в *ппропдата*, в байтах.

</dd> <dt>

*пкбретурнед* \[ заполняет\]
</dt> <dd>

Получает число байтов, которые метод копирует в массив *ппропдата* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                              | Описание                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                     | Успешно.<br/>                                                         |
| <dl> <dt>**\_набор свойств \_ E \_ не поддерживается**</dt> </dl> | Набор свойств не поддерживается.<br/>                               |
| <dl> <dt>**идентификатор "E \_ prop" \_ \_ не поддерживается**</dt> </dl>  | Идентификатор свойства не поддерживается для указанного набора свойств.<br/> |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Другой интерфейс с таким именем существует в файле заголовка дсаунд. h. Два интерфейса несовместимы. интерфейс [иксконтрол](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , документированный в DirectShow DDK, теперь является рекомендуемым интерфейсом для передачи наборов свойств между драйверами WDM и компонентами пользовательского режима.

 

Чтобы получить свойство, выделите буфер, который затем будет заполняться этим методом. Чтобы определить необходимый размер буфера, укажите **значение NULL** для *ппропдата* и ноль (0) для *кбпропдата*. Этот метод возвращает необходимый размер буфера в *пкбретурнед*.

Перед Кспрокси. h необходимо включить KS. h.

## <a name="examples"></a>Примеры

В следующем примере запрашивается ПИН-код для своей категории ПИН-кода путем извлечения свойства **ампроперти \_ PIN \_ Category** . (См. раздел [закрепить набор свойств](pin-property-set.md).)


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
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

[**Интерфейс Икспропертисет**](ikspropertyset.md)
</dt> <dt>

[Наборы свойств](property-sets.md)
</dt> </dl>

 

 
