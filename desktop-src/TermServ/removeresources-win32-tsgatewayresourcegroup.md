---
title: Метод Ремовересаурцес класса Win32_TSGatewayResourceGroup
description: Удаляет ресурсы из группы ресурсов.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовересаурцес
- Службы удаленных рабочих столов метода Ремовересаурцес, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Ремовересаурцес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e852f2994c3302e4e53f316496b023c9e8fc115508ff522f384aa4701d2050ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127519"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Метод Ремовересаурцес \_ класса Win32 тсгатевайресаурцеграуп

Удаляет ресурсы из группы ресурсов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ресурсы* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список ресурсов для удаления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Если в параметре *Resources* указано несколько ресурсов и один из ресурсов не может быть обработан, никакие ресурсы не будут обработаны.

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

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

