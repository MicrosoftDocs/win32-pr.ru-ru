---
title: Метод Сетсессиондиректорипроперти класса Win32_TSSessionDirectory
description: Задает свойство Сессиондиректорилокатион или свойство Сессиондиректориклустернаме для класса.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессиондиректорипроперти
- Службы удаленных рабочих столов метода Сетсессиондиректорипроперти, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сетсессиондиректорипроперти
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490083"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a>Метод Сетсессиондиректорипроперти \_ класса Win32 тссессиондиректори

Задает свойство **сессиондиректорилокатион** или свойство **сессиондиректориклустернаме** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropertyName* \[ окне\]
</dt> <dd>

Тип: **строка**

Указывает свойство, которое задается методом.

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**сессиондиректорилокатион**


</dt> <dd>

Метод устанавливает свойство **сессиондиректорилокатион** .

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**сессиондиректориклустернаме**


</dt> <dd>

Метод устанавливает свойство **сессиондиректориклустернаме** .

</dd> </dl> </dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Тип: **строка**

Новое значение для свойства, указанного параметром *PropertyName* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

