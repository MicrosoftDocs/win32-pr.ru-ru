---
title: Метод СетлоадбаланЦингстате класса Win32_TSSessionDirectory
description: Задает значение, указывающее, будет ли сервер участвовать в балансировке нагрузки подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода СетлоадбаланЦингстате
- Службы удаленных рабочих столов метода СетлоадбаланЦингстате, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод СетлоадбаланЦингстате
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d539f07c97e4e5b92152190a7bb38a8132d31a73daf08de8f140a39f67efdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987954"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Метод СетлоадбаланЦингстате \_ класса Win32 тссессиондиректори

Задает значение, указывающее, будет ли сервер участвовать в балансировке нагрузки подключение к удаленному рабочему столу Broker (RDCB).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Статевалуе* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Указывает, будет ли сервер участвовать в балансировке нагрузки RDCB.

<dt>

0
</dt> <dd>

Сервер не будет участвовать в балансировке нагрузки RDCB.

</dd> <dt>

1
</dt> <dd>

Сервер будет участвовать в балансировке нагрузки RDCB.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Сервер должен быть присоединен к ферме в RDCB.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

