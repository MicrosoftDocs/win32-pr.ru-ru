---
title: Метод Сетпромптфорпассворд класса Win32_TSLogonSetting
description: Метод Сетпромптфорпассворд задает свойство Промптфорпассворд.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпромптфорпассворд
- Службы удаленных рабочих столов метода Сетпромптфорпассворд, класс Win32_TSLogonSetting
- Класс Win32_TSLogonSetting службы удаленных рабочих столов, метод Сетпромптфорпассворд
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ea5202b0cfdfb624a05240deb042a88a8c73c8ea994cd810e1d9680ac0ddc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769524"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Метод Сетпромптфорпассворд \_ класса Win32 тслогонсеттинг

Метод **сетпромптфорпассворд** задает свойство **промптфорпассворд** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Промптфорпассворд* \[ окне\]
</dt> <dd>

Флаг отключения или включения свойства **промптфорпассворд** .

<dt>

0
</dt> <dd>

Отключает запрос пароля.

</dd> <dt>

1
</dt> <dd>

Включает запрос пароля.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

<dl> <dt>

**False** (0)
</dt> <dt>

**True** (1)
</dt> </dl>

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслогонсеттинг Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

