---
title: Метод Рефрешцертконтекст класса Win32_TSGatewayServerSettings
description: Обновляет сертификат, используемый сервером шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: caefeb85-1c7a-4868-9ee8-10ab09354595
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рефрешцертконтекст
- Службы удаленных рабочих столов метода Рефрешцертконтекст, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Рефрешцертконтекст
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RefreshCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81d25944e77a2c80c3f7823283cf0bef813ab51600a1a0a5f3b8aaf9dfb8eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769674"
---
# <a name="refreshcertcontext-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Рефрешцертконтекст \_ класса Win32 тсгатевайсерверсеттингс

Обновляет сертификат, используемый сервером шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 RefreshCertContext(
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

