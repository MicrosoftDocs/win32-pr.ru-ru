---
title: Метод Сетполиципропертинаме класса Win32_TerminalServiceSetting
description: Метод Сетполиципропертинаме задает свойство Делететемпфолдерс, Усетемпфолдерс или Help для класса.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетполиципропертинаме
- Службы удаленных рабочих столов метода Сетполиципропертинаме, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетполиципропертинаме
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a9009a05cb1c8de210c3e274af0e8c21297e9e01ed28dbc0c01d38edc06fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769984"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Метод Сетполиципропертинаме \_ класса Win32 терминалсервицесеттинг

Метод **сетполиципропертинаме** задает свойство **делететемпфолдерс**, **усетемпфолдерс** или **Help** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropertyName* \[ окне\]
</dt> <dd>

Задает свойство политики, которое задается методом.

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**делететемпфолдерс**


</dt> <dd>

Метод устанавливает свойство **делететемпфолдерс** .

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**усетемпфолдерс**


</dt> <dd>

Метод устанавливает свойство **усетемпфолдерс** .

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**Справка**


</dt> <dd>

Метод задает свойство **Help** .

**Справка по** **заметкам** не поддерживается  

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

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Remarks

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

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

