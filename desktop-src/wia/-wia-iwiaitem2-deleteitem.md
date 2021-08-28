---
description: Удаляет текущий объект IWiaItem2 из дерева объектов устройства.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: 'IWiaItem2: метод:D Елетеитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593004"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2: метод:D Елетеитем

Удаляет текущий объект [**IWiaItem2**](-wia-iwiaitem2.md) из дерева объектов устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

система времени выполнения Windows Image connect (wia) 2,0 представляет каждое устройство wia 2,0, подключенное к компьютеру пользователя, в виде иерархического дерева объектов [**IWiaItem2**](-wia-iwiaitem2.md) . Данное устройство WIA 2,0 может не позволить приложениям удалять объекты **IWiaItem2** из своего дерева. Элементы, имеющие дочерние объекты, не могут быть удалены. Интерфейс [**иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) должен использоваться для запроса устройства для возможности удаления элементов.

Если устройство поддерживает удаление элементов в дереве [**IWiaItem2**](-wia-iwiaitem2.md) , вызовите метод **IWiaItem2::D елетеитем** , чтобы удалить объект **IWiaItem2** . Обратите внимание, что этот метод удаляет объект только после освобождения всех ссылок на объект. Если удаление элемента завершилось сбоем, \_ возвращается E DELETEITEM. Числовое значение для этой ошибки еще не определено.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




