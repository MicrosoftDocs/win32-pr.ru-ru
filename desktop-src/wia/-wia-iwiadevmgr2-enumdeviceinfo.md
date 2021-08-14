---
description: создает перечислитель сведений о свойстве для каждого доступного устройства Windowsного получения изображений (WIA) 2,0.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'Метод IWiaDevMgr2:: Енумдевицеинфо (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8b646c494d9793986373d45db2d89dfde91e744196d86d28aceab35874f504d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208726"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>Метод IWiaDevMgr2:: Енумдевицеинфо

создает перечислитель сведений о свойстве для каждого доступного устройства Windowsного получения изображений (WIA) 2,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

Указывает тип устройств WIA 2,0 для перечисления.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DEVINFO \_ Enum \_ Local**


</dt> <dd>

Перечисляются только локально подключенные активные устройства проверки.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ Перечисление \_ ALL**


</dt> <dd>

Все устройства перечисляются как локально, так и удаленно, включая неактивные (отключенные) устройства и устаревшие устройства сти.

</dd> </dl> </dd> <dt>

*ппиенум* \[ out, retval\]
</dt> <dd>

Тип: **[ **иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Получает адрес указателя на интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Метод **IWiaDevMgr2:: енумдевицеинфо** создает объект перечислителя, поддерживающий интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Метод сохраняет указатель на интерфейс **иенумвиа \_ dev \_ info** в параметре *ппиенум*. Приложения могут использовать указатель интерфейса **иенумвиа \_ dev \_ info** для ПЕРЕЧИСЛЕНИЯ свойств каждого устройства WIA 2,0, подключенного к компьютеру пользователя.

Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппиенум* .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
