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
ms.openlocfilehash: edfb65ea7429af14e633c8dee655b4977427e3a685e1404856fd9b5f2daf2ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099574"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





