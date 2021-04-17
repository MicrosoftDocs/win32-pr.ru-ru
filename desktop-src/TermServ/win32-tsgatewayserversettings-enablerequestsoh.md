---
title: Метод Енаблерекуестсох класса Win32_TSGatewayServerSettings
description: Енаблерекуестсох больше не доступен.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблерекуестсох
- Службы удаленных рабочих столов метода Енаблерекуестсох, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблерекуестсох
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672820"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Енаблерекуестсох \_ класса Win32 тсгатевайсерверсеттингс

\[Метод **енаблерекуестсох** больше не доступен в Windows Server 2016.\]

Включает или отключает запросы состояния работоспособности (SoH).

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рекуестсох* \[ окне\]
</dt> <dd>

Укажите **значение true** , чтобы включить функцию, или **значение false** , чтобы отключить эту функцию.

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
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

