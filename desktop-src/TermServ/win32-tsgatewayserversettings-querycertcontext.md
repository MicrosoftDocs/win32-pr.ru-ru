---
title: Метод Куерицертконтекст класса Win32_TSGatewayServerSettings
description: Указывает, установлен ли указанный сертификат.
ms.assetid: 25d56f72-befd-46b4-84ff-dca748eeaca4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Куерицертконтекст
- Службы удаленных рабочих столов метода Куерицертконтекст, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Куерицертконтекст
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.QueryCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e158b348debc610682380d793b66949c5a7648
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492708"
---
# <a name="querycertcontext-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Куерицертконтекст \_ класса Win32 тсгатевайсерверсеттингс

Указывает, установлен ли указанный сертификат.

## <a name="syntax"></a>Синтаксис


```mof
uint32 QueryCertContext(
  [out] uint8 CertHash[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*CertHash* \[ заполняет\]
</dt> <dd>

Хэш сертификата, используемого сервером шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

