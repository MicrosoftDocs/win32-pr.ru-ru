---
description: Возвращает компонент предварительной версии для получения образа Windows (WIA) 2,0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'Метод IWiaItem2:: Жетпревиевкомпонент (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145409"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>Метод IWiaItem2:: Жетпревиевкомпонент

Возвращает компонент предварительной версии для получения образа Windows (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

Не используется. Задайте значение 0.

</dd> <dt>

*ппвиапревиев* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивиапревиев**](-wia-iwiapreview.md)\*\***

Возвращает адрес указателя на интерфейс [**ивиапревиев**](-wia-iwiapreview.md) компонента предварительной версии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция используется для возвращения указателя на адрес компонента предварительной версии WIA 2,0 для любого объекта [**IWiaItem2**](-wia-iwiaitem2.md) в дереве объектов аппаратного устройства WIA 2,0.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают через параметр *ппвиапревиев* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**ивиапревиев**](-wia-iwiapreview.md)
</dt> </dl>

 

 
