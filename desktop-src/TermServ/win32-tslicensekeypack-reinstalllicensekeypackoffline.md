---
title: Метод Реинсталллиценсекэйпаккоффлине класса Win32_TSLicenseKeyPack
description: Переустанавливает пакет лицензионного ключа службы удаленных рабочих столов, который использует идентификатор лицензии, полученный через Интернет или по телефону.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реинсталллиценсекэйпаккоффлине
- Службы удаленных рабочих столов метода Реинсталллиценсекэйпаккоффлине, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Реинсталллиценсекэйпаккоффлине
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b72ad2175e0d97cba5733461431726781aebc9a53c1a23f408f7d14e75dd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058332"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Метод Реинсталллиценсекэйпаккоффлине \_ класса Win32 тслиценсекэйпакк

Переустанавливает пакет лицензионного ключа службы удаленных рабочих столов, который использует идентификатор лицензии, полученный через Интернет или по телефону.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*слиценсекэйпаккид* \[ окне\]
</dt> <dd>

Содержит 35-символьный код лицензии. В качестве входных данных должна быть указана только строка, состоящая из 35 символов. Переносы не добавляются.

</dd> <dt>

*Кэйпаккид* \[ заполняет\]
</dt> <dd>

Получает идентификатор пакета ключей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requirements (Требования)



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

 

 





