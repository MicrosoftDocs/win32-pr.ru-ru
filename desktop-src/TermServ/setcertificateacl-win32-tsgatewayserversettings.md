---
title: Метод Сетцертификатеакл класса Win32_TSGatewayServerSettings
description: Задает сертификат, необходимый для доступа к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 274c24bf-4e44-42ea-a109-99d0249c2f78
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетцертификатеакл
- Службы удаленных рабочих столов метода Сетцертификатеакл, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетцертификатеакл
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificateACL
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc18dd0bf72ac63216e71e1a7db6a133d6a97f79d3a62876f8a9c9458007e25d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138037"
---
# <a name="setcertificateacl-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Сетцертификатеакл \_ класса Win32 тсгатевайсерверсеттингс

Задает сертификат, необходимый для доступа к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetCertificateACL(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*CertHash* \[ окне\]
</dt> <dd>

Хэш сертификата, используемого сервером шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

