---
description: Метод Reset \_ класса CIM поинтингдевице запрашивает сброс логического устройства.
ms.assetid: c7479e34-c95a-4eac-847c-3637f493ee9f
ms.tgt_platform: multiple
title: Метод Reset класса CIM_PointingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33ee82189909b2d04626f584a792c0c06275d2dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807469"
---
# <a name="reset-method-of-the-cim_pointingdevice-class"></a>Метод Reset \_ класса CIM поинтингдевице

Метод **Reset** \_ класса CIM поинтингдевице запрашивает сброс логического устройства. Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 Reset();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.

## <a name="remarks"></a>Комментарии

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

[\_ПОИНТИНГДЕВИЦЕ CIM](reset-method-in-class-cim-pointingdevice.md)
</dt> <dt>

[**\_ПОИНТИНГДЕВИЦЕ CIM**](cim-pointingdevice.md)
</dt> </dl>

 

 




