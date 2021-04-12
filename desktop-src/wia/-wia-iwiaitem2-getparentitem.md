---
description: Возвращает родительский элемент в дереве, который представляет устройство с аппаратным обеспечением Windows для получения образа (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'Метод IWiaItem2:: Жетпарентитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343665"
---
# <a name="iwiaitem2getparentitem-method"></a>Метод IWiaItem2:: Жетпарентитем

Возвращает родительский элемент в дереве, который представляет устройство с аппаратным обеспечением Windows для получения образа (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ppIWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) родителя элемента в дереве объектов элементов. Если этот метод вызывается в корне дерева, возвращенный адрес имеет **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

При наличии объекта [**IWiaItem2**](-wia-iwiaitem2.md) в дереве объектов аппаратного устройства WIA 2,0 приложение получает указатель на родительский элемент, вызывая эту функцию.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают через параметр *ppIWiaItem2* , если эти указатели не **равны NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
