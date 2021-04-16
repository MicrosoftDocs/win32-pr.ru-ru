---
title: Метод Сетмаксмониторс класса Win32_TSClientSetting
description: Задает свойство Максмониторс.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетмаксмониторс
- Службы удаленных рабочих столов метода Сетмаксмониторс, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетмаксмониторс
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672712"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Метод Сетмаксмониторс \_ класса Win32 тсклиентсеттинг

Задает свойство **максмониторс** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Максмониторс* \[ окне\]
</dt> <dd>

Указывает новое максимальное число мониторов, поддерживаемое сервером. Минимальное значение равно 1, а максимальное значение — 10.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметры соединения пользователя переопределяются сервером.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсклиентсеттинг Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

 





