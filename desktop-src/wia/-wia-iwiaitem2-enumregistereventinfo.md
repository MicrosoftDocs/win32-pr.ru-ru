---
description: 'Метод IWiaItem2:: Енумрегистеревентинфо создает перечислитель, который можно использовать для получения сведений о событиях, для которых зарегистрировано приложение.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'Метод IWiaItem2:: Енумрегистеревентинфо (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145418"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>Метод IWiaItem2:: Енумрегистеревентинфо

Метод **IWiaItem2:: енумрегистеревентинфо** создает перечислитель, который можно использовать для получения сведений о событиях, для которых зарегистрировано приложение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

Не используется. Задайте значение 0.

</dd> <dt>

*певентгуид* \[ окне\]
</dt> <dd>

Тип: **константа \* GUID* _

Указатель на идентификатор, указывающий событие оборудования, для которого требуется получить сведения о регистрации.

</dd> <dt>

_ppIEnum * \[ out\]
</dt> <dd>

Тип: **[ **иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Адрес указателя на интерфейс [**\_ \_ Caps иенумвиа dev**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Приложение вызывает этот метод для создания объекта перечислителя для сведений о событии. **IWiaItem2:: енумрегистеревентинфо** сохраняет адрес интерфейса [**\_ \_ Caps иенумвиа dev**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) объекта перечислителя в параметре *ппиенум* . Затем программа использует указатель интерфейса для перечисления свойств события, для которого оно зарегистрировано.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают через параметр *ппиенум* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
