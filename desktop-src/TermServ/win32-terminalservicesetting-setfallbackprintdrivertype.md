---
title: Метод Сетфаллбаккпринтдривертипе класса Win32_TerminalServiceSetting
description: Метод Сетфаллбаккпринтдривертипе задает свойство Фаллбаккпринтдривертипе для класса.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетфаллбаккпринтдривертипе
- Службы удаленных рабочих столов метода Сетфаллбаккпринтдривертипе, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетфаллбаккпринтдривертипе
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071946"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Метод Сетфаллбаккпринтдривертипе \_ класса Win32 терминалсервицесеттинг

Метод **сетфаллбаккпринтдривертипе** задает свойство **фаллбаккпринтдривертипе** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фаллбаккпринтдривертипе* \[ окне\]
</dt> <dd>

Задает свойство **фаллбаккпринтдривертипе** , которое разрешает или запрещает новые подключения службы удаленных рабочих столов.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Нет резервных драйверов.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Лучшее предположение.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Лучшее предположение. Если совпадений не найдено, откат к Hewlett-Packard языку управления принтера (PCL).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

Лучшее предположение. Если совпадений не найдено, возвращается резервный вариант в PostScript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**четырех**


</dt> <dd>

Лучшее предположение. Если совпадений не найдено, отобразите драйверы PS и PCL.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

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

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

