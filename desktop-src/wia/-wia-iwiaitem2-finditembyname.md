---
description: Выполняет поиск в дереве элементов подэлементов, используя имя в качестве ключа поиска.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'Метод IWiaItem2:: Финдитембинаме (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5ef0ffdf710d36d2d6c515352bf441e9c66ae169400528db5d5943e2114fefd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440412"
---
# <a name="iwiaitem2finditembyname-method"></a>Метод IWiaItem2:: Финдитембинаме

Выполняет поиск в дереве элементов подэлементов, используя имя в качестве ключа поиска.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*бстрфуллитемнаме* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает имя искомого элемента.

</dd> <dt>

*ppIWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) найденного элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод выполняет поиск в дереве элементов текущего элемента, используя имя в качестве ключа поиска. Если **IWiaItem2:: финдитембинаме** находит элемент, указанный в *бстрфуллитемнаме*, он сохраняет адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) элемента в параметре *ppIWiaItem2* .

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
