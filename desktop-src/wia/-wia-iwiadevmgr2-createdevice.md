---
description: создает иерархическое дерево объектов IWiaItem2 для устройства Windowsного получения изображений (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'Метод IWiaDevMgr2:: Креатедевице (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a40267e77671b807f0e6969845a3a5a7096694e4f4e7978467ee9ca5909284d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965733"
---
# <a name="iwiadevmgr2createdevice-method"></a>Метод IWiaDevMgr2:: Креатедевице

создает иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) для устройства Windowsного получения изображений (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает уникальный идентификатор устройства WIA 2,0.

</dd> <dt>

*ppWiaItem2Root* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) корневого элемента в иерархическом дереве для устройства WIA 2,0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Приложения используют метод **IWiaDevMgr2:: креатедевице** для создания объекта устройства для устройств WIA 2,0, заданных параметром бстрдевицеид. При возврате метод **IWiaDevMgr2:: креатедевице** сохраняет адрес указателя в параметре *ppWiaItem2Root*, который указывает на корневой элемент дерева объектов [**IWiaItem2**](-wia-iwiaitem2.md) , созданных **IWiaDevMgr2:: креатедевице**. Приложения могут использовать это дерево объектов для управления и извлечения данных с устройства WIA 2,0.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей, которые они получают с помощью параметра *ppWiaItem2Root* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
