---
title: Метод Реинсталлретаилпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по розничному каналу.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реинсталлретаилпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Реинсталлретаилпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Реинсталлретаилпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071215"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Метод Реинсталлретаилпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк

Переустанавливает пакет лицензионных ключей службы удаленных рабочих столов, приобретенный по розничному каналу.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*слиценсекоде* \[ окне\]
</dt> <dd>

Содержит 25-символьный код лицензии. В качестве входных данных должно быть задано только 25-символьная строка символов. Переносы не добавляются.

</dd> <dt>

*Кэйпаккид* \[ заполняет\]
</dt> <dd>

Получает идентификатор пакета ключей.

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





