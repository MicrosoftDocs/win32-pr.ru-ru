---
description: Возвращает корневой элемент дерева объектов элементов, используемых для представления аппаратного устройства для получения образа Windows (WIA) 2,0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'Метод IWiaItem2:: Жетрутитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809983"
---
# <a name="iwiaitem2getrootitem-method"></a>Метод IWiaItem2:: Жетрутитем

Возвращает корневой элемент дерева объектов элементов, используемых для представления аппаратного устройства для получения образа Windows (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ppIWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) корневого элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

При наличии объекта [**IWiaItem2**](-wia-iwiaitem2.md) в дереве объектов аппаратного устройства WIA 2,0 приложение получает указатель на корневой элемент, вызывая эту функцию.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
