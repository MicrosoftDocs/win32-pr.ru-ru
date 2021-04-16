---
title: Метод Ремовевиртуалдесктоп класса Win32_RDMSVirtualDesktopCollection
description: Удаляет виртуальный рабочий стол из коллекции виртуальных рабочих столов.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовевиртуалдесктоп
- Службы удаленных рабочих столов метода Ремовевиртуалдесктоп, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Ремовевиртуалдесктоп
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a468de22d571fa52d37c2ad51d40d492af35384a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533914"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Ремовевиртуалдесктоп \_ класса Win32 рдмсвиртуалдесктопколлектион

Удаляет виртуальный рабочий стол из коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*VMName* \[ окне\]
</dt> <dd>

Имя виртуальной машины, на которой размещен виртуальный рабочий стол.

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

 

 





