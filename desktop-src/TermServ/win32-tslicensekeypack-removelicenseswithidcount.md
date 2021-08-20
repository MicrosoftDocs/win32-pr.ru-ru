---
title: Метод Ремовелиценсесвисидкаунт класса Win32_TSLicenseKeyPack
description: Удаляет указанное число лицензий службы удаленных рабочих столов из указанного пакета ключей.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовелиценсесвисидкаунт
- Службы удаленных рабочих столов метода Ремовелиценсесвисидкаунт, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Ремовелиценсесвисидкаунт
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7cf3c5b47a68828fc4c4d35d682f9d1a79491e7b1b76489d0d1385ea765ccc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940004"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a>Метод Ремовелиценсесвисидкаунт \_ класса Win32 тслиценсекэйпакк

Удаляет указанное число лицензий службы удаленных рабочих столов из указанного пакета ключей.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кэйпаккид* \[ окне\]
</dt> <dd>

Идентификатор пакета ключей, содержащего удаляемые лицензии.

</dd> <dt>

*Лиценсекаунт* \[ окне\]
</dt> <dd>

Число удаляемых лицензий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





