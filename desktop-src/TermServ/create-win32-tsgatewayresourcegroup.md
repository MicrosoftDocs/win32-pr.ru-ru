---
title: Метод Create класса Win32_TSGatewayResourceGroup
description: Создает группу ресурсов.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_TSGatewayResourceGroup класса
- Класс Win32_TSGatewayResourceGroup службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e4de66eff704ab5d061dcb7675c1ab4ef9d847e5e7235e872f5872b8f3376fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871754"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a>Метод Create \_ класса Win32 тсгатевайресаурцеграуп

Создает группу ресурсов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Имя группы ресурсов.

</dd> <dt>

*Описание* \[ окне\]
</dt> <dd>

Описание группы ресурсов.

</dd> <dt>

*Ресурсы* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список ресурсов в этой группе ресурсов. " \* " Означает все ресурсы.

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

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

