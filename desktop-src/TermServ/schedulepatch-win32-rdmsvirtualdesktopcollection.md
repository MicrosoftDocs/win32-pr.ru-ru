---
title: Метод Счедулепатч класса Win32_RDMSVirtualDesktopCollection
description: Планирует задание подготовки обновлений программного обеспечения, устанавливающее обновления программного обеспечения на виртуальных машинах в коллекции виртуальных рабочих столов.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Счедулепатч
- Службы удаленных рабочих столов метода Счедулепатч, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Счедулепатч
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490314"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Счедулепатч \_ класса Win32 рдмсвиртуалдесктопколлектион

Планирует задание подготовки обновлений программного обеспечения, устанавливающее обновления программного обеспечения на виртуальных машинах в коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

Время *начала* \[ окне\]
</dt> <dd>

> [!Note]  
> Система не выполнит выход пользователей виртуальных машин до тех пор, пока не будет указано значение параметра *форцелогоффтиме* .

 

Дата и время установки обновлений.

</dd> <dt>

*Форцелогоффтиме* \[ окне\]
</dt> <dd>

Дата и время, когда система будет выходить из системы пользователей виртуальных машин.

</dd> <dt>

*Жобинпутксмл* \[ окне\]
</dt> <dd>

Строка в формате XML, содержащая сведения о задании обновления программного обеспечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





