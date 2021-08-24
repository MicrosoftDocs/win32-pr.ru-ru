---
description: Метод StartService класса CIM_Service (поставщики WMI CIMWin32) — метод StartService помещает службу в запущенное состояние.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Метод StartService класса CIM_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87fcdad650ea93461850bab3e3e66d9543025a2b468b9f7948f6d949d5838c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752444"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a>Метод StartService класса CIM_Service (поставщики WMI CIMWin32)

Метод **StartService** помещает службу в запущенное состояние.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 StartService();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки. В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе. Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .

## <a name="remarks"></a>Remarks

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_Служба CIM](startservice-method-in-class-cim-service.md)
</dt> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

