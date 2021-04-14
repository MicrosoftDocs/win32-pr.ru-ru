---
title: Метод Сетресаурцес класса Win32_TSGatewayResourceGroup
description: Задает свойство Resources для этой группы ресурсов.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетресаурцес
- Службы удаленных рабочих столов метода Сетресаурцес, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Сетресаурцес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415149"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Метод Сетресаурцес \_ класса Win32 тсгатевайресаурцеграуп

Задает свойство **Resources** для этой группы ресурсов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ресурсы* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список ресурсов в этой группе ресурсов. " \* " Означает все ресурсы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Если в параметре *Resources* указано несколько ресурсов и один из ресурсов не может быть обработан, никакие ресурсы не будут обработаны.

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

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

