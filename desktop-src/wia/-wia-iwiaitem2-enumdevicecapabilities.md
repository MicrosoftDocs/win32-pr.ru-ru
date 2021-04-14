---
description: Создает перечислитель, который используется для определения команд и событий, которые поддерживает устройство для получения изображений (WIA) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'Метод IWiaItem2:: Енумдевицекапабилитиес (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541983"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>Метод IWiaItem2:: Енумдевицекапабилитиес

Создает перечислитель, который используется для определения команд и событий, которые поддерживает устройство для получения изображений (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

Указывает флаг, выбирающий тип возможностей для перечисления. Это одно из следующих значений.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_команды устройства \_ WIA**


</dt> <dd>

Перечисление команд устройств.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_события устройства \_ WIA**


</dt> <dd>

Перечисление событий устройства.

</dd> </dl> </dd> <dt>

*ппиенумвиа \_ \_Ограничения разработки* \[\]
</dt> <dd>

Тип: **[ **иенумвиа \_ dev \_ Cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Получает указатель на интерфейс [**\_ \_ Caps dev иенумвиа**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) , созданный этим методом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод используется для создания объекта перечислителя для получения набора команд и событий, поддерживаемых устройством WIA 2,0. Параметр *лфлагс* используется для указания типов возможностей устройства для перечисления. Метод **IWiaItem2:: енумдевицекапабилитиес** сохраняет адрес интерфейса объекта перечислителя в параметре *ппиенумвиа \_ dev \_ Cap* .

Этот метод может быть вызван только для корневого элемента объектов [**IWiaItem2**](-wia-iwiaitem2.md) дерева устройств.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенумвиа \_ dev \_ Caps* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
