---
title: Метод ИслоадбаланЦингсервер класса Win32_TSGatewayLoadBalancer
description: Определяет, может ли сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) выполнять балансировку нагрузки.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ИслоадбаланЦингсервер
- Службы удаленных рабочих столов метода ИслоадбаланЦингсервер, класс Win32_TSGatewayLoadBalancer
- Класс Win32_TSGatewayLoadBalancer службы удаленных рабочих столов, метод ИслоадбаланЦингсервер
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681958"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a>Метод ИслоадбаланЦингсервер \_ класса Win32 тсгатевайлоадбаланцер

Определяет, может ли сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов) выполнять балансировку нагрузки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*LoadBalancing* \[ заполняет\]
</dt> <dd>

**Значение true** , если сервер может выполнять балансировку нагрузки, и **false** в противном случае.

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

[**\_Тсгатевайлоадбаланцер Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

