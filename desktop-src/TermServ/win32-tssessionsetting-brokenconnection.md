---
title: Метод Брокенконнектион класса Win32_TSSessionSetting (Втспротокол. h)
description: Задает свойство Брокенконнектионактион, которое является действием, которое сервер принимает, если достигнуто предельное время сеанса или если соединение разорвано.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Брокенконнектион
- Службы удаленных рабочих столов метода Брокенконнектион, класс Win32_TSSessionSetting
- Класс Win32_TSSessionSetting службы удаленных рабочих столов, метод Брокенконнектион
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681864"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Метод Брокенконнектион \_ класса Win32 тссессионсеттинг

Задает свойство **брокенконнектионактион** , которое является действием, которое сервер принимает, если достигнуто предельное время сеанса или если соединение разорвано.

## <a name="syntax"></a>Синтаксис


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Брокенконнектионактион* \[ окне\]
</dt> <dd>

Предпринимаемое действие.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Отключить** (0)


</dt> <dd>

Пользователь отключен от сеанса.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (1)


</dt> <dd>

Сеанс окончательно удаляется с сервера.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в элементе управления групповая политика.

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| Header<br/>                   | <dl> <dt>Втспротокол. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тссессионсеттинг Win32**](win32-tssessionsetting.md)
</dt> </dl>

 

