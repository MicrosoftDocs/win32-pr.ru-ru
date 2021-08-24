---
title: Метод Енаблеусервхд класса Win32_TSSessionDirectory
description: Включает виртуальный жесткий диск профиля пользователя на сервере узлов удаленных рабочих столов.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблеусервхд
- Службы удаленных рабочих столов метода Енаблеусервхд, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Енаблеусервхд
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19e042b51c7060e4d4c2a8302a87b2d27ee2cf89608a9831cb3497fd0566689a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871744"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Метод Енаблеусервхд \_ класса Win32 тссессиондиректори

Включает виртуальный жесткий диск профиля пользователя на сервере узлов удаленных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Увхдшареурл* \[ окне\]
</dt> <dd>

Расположение общей папки, в которой хранятся все виртуальные жесткие диски профиля пользователя.

</dd> <dt>

*Увхдроамингполициксмл* \[ окне\]
</dt> <dd>

Политика роуминга для виртуального жесткого диска профиля пользователя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





