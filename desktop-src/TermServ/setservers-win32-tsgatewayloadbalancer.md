---
title: Метод Сетсерверс класса Win32_TSGatewayLoadBalancer
description: Задает свойство Servers со списком серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсерверс
- Службы удаленных рабочих столов метода Сетсерверс, класс Win32_TSGatewayLoadBalancer
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов, метод Сетсерверс
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c23ac6cf965687a022c5ae5ba8c1ce690c39c45f9149076f36ab13bc2d222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349624"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Метод Сетсерверс \_ класса Win32 тсгатевайлоадбаланцер

Задает свойство **Servers** со списком серверов балансировки нагрузки шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Серверы* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список серверов балансировки нагрузки шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Если в параметре *Servers* указано несколько серверов, и один из серверов не может быть обработан, никакие серверы не будут обработаны.

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

[**\_Тсгатевайлоадбаланцер Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

