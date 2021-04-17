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
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692522"
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

Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Указатель на [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) передаваемого элемента. Этот объект минимальное реализует [_ *IWiaItem2* *](-wia-iwiaitem2.md) и [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

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

Тип: **Byte \** _

Указатель на буфер данных, полученный с помощью [_ *бандеддатакаллбакк* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*пбстрдескриптион* \[ заполняет\]
</dt> <dd>

Тип: **BSTR \** _

_ *BSTR**, которая получает описание состояния или ошибки, возникшей во время передачи данных. Этот параметр не может иметь **значение NULL**. Вызывающий объект должен освободить строку с помощью [сисфристринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), и разработчик должен выделить строку с помощью [сисаллокстринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает одно из следующих значений.



| Код возврата                                                                             | Описание                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | *пбстрдескриптион* содержит допустимый указатель **BSTR** . <br/>  |
| <dl> <dt>**S \_ false**</dt> </dl> | *хрстатус* неизвестен, и описание недоступно. <br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



 

 
