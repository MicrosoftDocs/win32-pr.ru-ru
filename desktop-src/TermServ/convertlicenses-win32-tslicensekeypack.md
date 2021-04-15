---
title: Метод Конвертлиценсес класса Win32_TSLicenseKeyPack
description: Преобразует лицензии в текущем ключевом пакете.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Конвертлиценсес
- Службы удаленных рабочих столов метода Конвертлиценсес, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Конвертлиценсес
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414956"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Метод Конвертлиценсес \_ класса Win32 тслиценсекэйпакк

Преобразует лицензии в текущем ключевом пакете. Если лицензия является лицензией для каждого пользователя, она преобразуется в лицензию для каждого устройства. Если лицензия является лицензией для каждого устройства, она преобразуется в лицензию для каждого пользователя.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Количество* \[ окне\]
</dt> <dd>

Число лицензий для преобразования.

</dd> <dt>

*Кэйпаккид* \[ заполняет\]
</dt> <dd>

Идентификатор результирующего пакета ключей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





