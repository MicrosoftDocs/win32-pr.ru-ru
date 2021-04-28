---
description: Метод Reset класса CIM_MultiStateSensor. метод Reset запрашивает сброс логического устройства. Этот метод наследуется от CIM-ого модели \_ .
ms.assetid: 51234db3-496a-4750-a185-84a5945228b9
ms.tgt_platform: multiple
title: Метод Reset класса CIM_MultiStateSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MultiStateSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41694086537fac64cc5c6eb3019a079649c1b248
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096902"
---
# <a name="reset-method-of-the-cim_multistatesensor-class"></a>Метод Reset \_ класса CIM мултистатесенсор

Метод **Reset** запрашивает сброс логического устройства. Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[\_МУЛТИСТАТЕСЕНСОР CIM](reset-method-in-class-cim-multistatesensor.md)
</dt> <dt>

[**\_МУЛТИСТАТЕСЕНСОР CIM**](cim-multistatesensor.md)
</dt> </dl>

 

 




