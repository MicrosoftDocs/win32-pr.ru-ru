---
title: Метод Тимелимит класса Win32_TSSessionSetting
description: Задает максимальное время, выделенное для указанного типа ограничения сеанса.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Тимелимит
- Службы удаленных рабочих столов метода Тимелимит, класс Win32_TSSessionSetting
- Класс Win32_TSSessionSetting службы удаленных рабочих столов, метод Тимелимит
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f49451b1f6b7b2e63079d0bebbcd0dbb43b76352ae3609ce4138b771a01e03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137557"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>Метод Тимелимит \_ класса Win32 тссессионсеттинг

Задает максимальное время, выделенное для указанного типа ограничения сеанса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сессионлимиттипе* \[ окне\]
</dt> <dd>

Указывает тип свойства ограничения сеанса, которое задается методом.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**активесессионлимит**


</dt> <dd>

Метод устанавливает свойство **активесессионлимит** .

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**дисконнектедсессионлимит**


</dt> <dd>

Метод устанавливает свойство **дисконнектедсессионлимит** .

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**идлесессионлимит**


</dt> <dd>

Метод устанавливает свойство **идлесессионлимит** .

</dd> </dl> </dd> <dt>

*ValueLimit* \[ окне\]
</dt> <dd>

Новое максимальное время в миллисекундах для свойства, указанного параметром *сессионлимиттипе* . Нулевое значение указывает на отсутствие ограничения сеанса.

</dd> </dl>

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

[**\_Тссессионсеттинг Win32**](win32-tssessionsetting.md)
</dt> </dl>

 

