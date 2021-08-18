---
title: Метод Ремотеконтрол класса Win32_TSRemoteControlSetting
description: Метод Ремотеконтрол задает свойство Левелофконтрол.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремотеконтрол
- Службы удаленных рабочих столов метода Ремотеконтрол, класс Win32_TSRemoteControlSetting
- Класс Win32_TSRemoteControlSetting службы удаленных рабочих столов, метод Ремотеконтрол
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73de3f92171f688a9c0dc611552a061a3f2de7bf573fa41dab8606395eafe228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769424"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Метод Ремотеконтрол \_ класса Win32 тсремотеконтролсеттинг

Метод **ремотеконтрол** задает свойство **левелофконтрол** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Левелофконтрол* \[ окне\]
</dt> <dd>

Новое значение свойства **левелофконтрол** , которое указывает, будет ли сеанс просматриваться только удаленным пользователем или просматриваться и контролироваться с помощью клавиатуры и мыши. Дополнительные сведения см. в разделе "Замечания". Поддерживаются следующие значения.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (0)


</dt> <dd>

Удаленное управление отключено.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**Енаблеинпутнотифи** (1)


</dt> <dd>

Пользователь удаленного управления имеет полный контроль над сеансом пользователя с разрешением пользователя.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**Енаблеинпутнонотифи** (2)


</dt> <dd>

Пользователь удаленного управления имеет полный контроль над сеансом пользователя; разрешение пользователя не требуется.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**Енабленоинпутнотифи** (3)


</dt> <dd>

Пользователь удаленного управления может просматривать сеанс удаленно с разрешением пользователя; удаленный пользователь не может активно управлять сеансом.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**Енабленоинпутнонотифи** (4)


</dt> <dd>

Пользователь удаленного управления может просматривать сеанс удаленно, но не управляет им активно. разрешение пользователя не требуется.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Remarks

Полный контроль над сеансом означает, что удаленный пользователь может активно управлять сеансом пользователя с помощью клавиатуры и мыши.

Когда пользователь пытается установить подключение удаленного управления, система отображает сообщение удаленному клиенту, запрашивая разрешение на просмотр или участие в активном сеансе.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсремотеконтролсеттинг Win32**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

