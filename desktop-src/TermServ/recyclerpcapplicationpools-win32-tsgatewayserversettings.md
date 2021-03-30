---
title: Метод Рециклерпкаппликатионпулс класса Win32_TSGatewayServerSettings
description: Повторное использование пулов приложений RPC в службах IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рециклерпкаппликатионпулс
- Службы удаленных рабочих столов метода Рециклерпкаппликатионпулс, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Рециклерпкаппликатионпулс
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490317"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a>Метод Рециклерпкаппликатионпулс \_ класса Win32 тсгатевайсерверсеттингс

Повторное использование пулов приложений RPC в службах IIS.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Вызов этого метода приводит к отключению всех существующих подключений.

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**сетаусентикатионплугин**](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

