---
title: Метод Сетклиентпроперти класса Win32_TSClientSetting
description: Метод Сетклиентпроперти задает свойство Лптпортмаппинг, Компортмаппинг, Аудиомаппинг, Клипбоардмаппинг, Дривемаппинг или WindowsPrinterMapping для класса.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетклиентпроперти
- Службы удаленных рабочих столов метода Сетклиентпроперти, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетклиентпроперти
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672629"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a>Метод Сетклиентпроперти \_ класса Win32 тсклиентсеттинг

Метод **сетклиентпроперти** задает свойство **лптпортмаппинг**, **компортмаппинг**, **аудиомаппинг**, **клипбоардмаппинг**, **дривемаппинг** или **WindowsPrinterMapping** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropertyName* \[ окне\]
</dt> <dd>

Указывает свойство клиента, для которого настраивается метод.

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**аудиомаппинг**


</dt> <dd>

Метод устанавливает свойство **аудиомаппинг** .

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**клипбоардмаппинг**


</dt> <dd>

Метод устанавливает свойство **клипбоардмаппинг** .

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**компортмаппинг**


</dt> <dd>

Метод устанавливает свойство **компортмаппинг** .

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**дривемаппинг**


</dt> <dd>

Метод устанавливает свойство **дривемаппинг** .

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**лптпортмаппинг**


</dt> <dd>

Метод устанавливает свойство **лптпортмаппинг** .

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**пнпредиректион**


</dt> <dd>

Метод устанавливает свойство **пнпредиректион** .

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**виндовспринтермаппинг**


</dt> <dd>

Метод устанавливает свойство **виндовспринтермаппинг** .

</dd> </dl> </dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Значение, указывающее, следует ли включать или отключать свойство, заданное параметром *PropertyName* .

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Отключите свойство.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Включите свойство.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если указанное свойство клиента не находится в элементе управления групповой политики или если параметр свойства не может переопределяться сервером.

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Тсклиентсеттинг Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

