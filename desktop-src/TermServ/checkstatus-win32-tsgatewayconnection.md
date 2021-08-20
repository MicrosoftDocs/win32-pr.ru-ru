---
title: Метод CheckStatus класса Win32_TSGatewayConnection
description: Проверяет состояние подключения сервера шлюза удаленный рабочий стол (удаленных рабочих столов) к другому компьютеру и определяет, настроен ли целевой компьютер для балансировки нагрузки.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода CheckStatus
- Службы удаленных рабочих столов метода CheckStatus, класс Win32_TSGatewayConnection
- Класс Win32_TSGatewayConnection службы удаленных рабочих столов, метод CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1056bbbd072a22310aa1c01cc92064819f13577018ed24c46e747f9a86b3566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942171"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>Метод CheckStatus \_ класса Win32 тсгатевайконнектион

Проверяет состояние подключения сервера шлюза удаленный рабочий стол (удаленных рабочих столов) к другому компьютеру и определяет, настроен ли целевой компьютер для балансировки нагрузки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя сервера* \[ окне\]
</dt> <dd>

Имя исходного сервера шлюза удаленных рабочих столов, с которого проверяется подключение.

</dd> <dt>

*EndPointName* \[ окне\]
</dt> <dd>

Имя целевого сервера (конечной точки), к которому проверяется доступ с исходного сервера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие возможные возвращаемые значения.

<dl> <dt>


</dt> <dd>

0

Состояние подключения — ОК. Конечная точка доступна и настроена для балансировки нагрузки.

</dd> <dt>


</dt> <dd>

1

Состояние подключения неизвестно. Скорее всего, возникло исключение.

</dd> <dt>


</dt> <dd>

0x80075c34

Конечная точка либо недоступна, либо не настроена для балансировки нагрузки.

</dd> <dt>


</dt> <dd>

0x80075c32

Произошла ошибка состояния. Конечная точка доступна, но служба балансировки нагрузки RPC/HTTP (РПЧТТПЛБС) не запущена на целевом компьютере.

</dd> </dl>

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайконнектион Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

