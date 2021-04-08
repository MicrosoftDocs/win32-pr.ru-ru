---
title: Метод SetName класса Win32_TSGatewayResourceGroup
description: Задает свойство Name для группы ресурсов.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetName
- Службы удаленных рабочих столов метода SetName, класс Win32_TSGatewayResourceGroup
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891933"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a>Метод SetName \_ класса Win32 тсгатевайресаурцеграуп

Задает свойство **Name** для группы ресурсов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Имя группы ресурсов. Имя должно содержать 64 символов или меньше, уникально (регистр игнорируется) и не может включать следующие зарезервированные символы:

<> :; " / \\ \| ? \*\[Вкладка\]

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

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

