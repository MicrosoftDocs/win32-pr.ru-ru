---
description: Возвращает строку, описывающую код состояния.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Метод Ивиаеррорхандлер:: Жетстатусдескриптион (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 963dc0059cf4fd45dffb0fc406cb6b2849aef456309cf15e80bf094c2ce01d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208306"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>Метод Ивиаеррорхандлер:: Жетстатусдескриптион

Возвращает строку, описывающую код состояния.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пункитем* \[ окне\]
</dt> <dd>

Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Указатель на [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) передаваемого элемента. Этот объект минимальное реализует [**IWiaItem2**](-wia-iwiaitem2.md) и [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*хрстатус* \[ окне\]
</dt> <dd>

Тип: **HRESULT**

**Значение HRESULT** , которое является кодом состояния, полученным [**бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*кбресленгс* \[ окне\]
</dt> <dd>

Тип: **Long**

Значение **типа Long** , равное размеру данных, на которые ссылается *pbData*.

</dd> <dt>

*pbData* \[ окне\]
</dt> <dd>

Тип: **Byte \***

Указатель на буфер данных, полученный [**бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*пбстрдескриптион* \[ заполняет\]
</dt> <dd>

Тип: **BSTR \***

**BSTR** , который получает описание состояния или ошибки, возникшей во время передачи данных. Этот параметр не может иметь **значение NULL**. Вызывающий объект должен освободить строку с помощью [сисфристринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), и разработчик должен выделить строку с помощью [сисаллокстринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает одно из следующих значений.



| Код возврата                                                                             | Описание                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | *пбстрдескриптион* содержит допустимый указатель **BSTR** . <br/>  |
| <dl> <dt>**S \_ false**</dt> </dl> | *хрстатус* неизвестен, и описание недоступно. <br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
