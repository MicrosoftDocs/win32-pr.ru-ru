---
title: Метод Инсталлретаилпурчаселиценсекэйпакк класса Win32_TSLicenseKeyPack
description: Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по розничному каналу.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инсталлретаилпурчаселиценсекэйпакк
- Службы удаленных рабочих столов метода Инсталлретаилпурчаселиценсекэйпакк, класс Win32_TSLicenseKeyPack
- Класс Win32_TSLicenseKeyPack службы удаленных рабочих столов, метод Инсталлретаилпурчаселиценсекэйпакк
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672538"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Метод Инсталлретаилпурчаселиценсекэйпакк \_ класса Win32 тслиценсекэйпакк

Устанавливает службы удаленных рабочих столов пакет лицензионных ключей, приобретенный по розничному каналу.

## <a name="syntax"></a>Синтаксис


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
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

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

