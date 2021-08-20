---
title: Метод Сетцертификате класса Win32_TSGatewayServerSettings
description: Задает хэш сертификата для привязки HTTPS через порт 443 в IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетцертификате
- Службы удаленных рабочих столов метода Сетцертификате, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетцертификате
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54b11f87e3cdc8c5c211f67e03a067690ddeac5ab3bc342794e1e97a8f339117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127479"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Сетцертификате \_ класса Win32 тсгатевайсерверсеттингс

Задает хэш сертификата для привязки HTTPS через порт 443 в IIS.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*CertHash* \[ окне\]
</dt> <dd>

Тип: **Uint8 \[ \]**

Новый хэш сертификата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

После того как хэш сертификата будет установлен с помощью этого метода, необходимо вызвать метод [**Configure**](configure-win32-tsgatewayserversettings.md) , чтобы завершить процесс настройки.

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

