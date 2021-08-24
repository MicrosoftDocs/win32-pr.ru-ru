---
description: Метод Reset \_ класса CIM пквидеоконтроллер запрашивает сброс логического устройства.
ms.assetid: 0dbed7af-6c7a-4bbb-b1ae-d768d2f88697
ms.tgt_platform: multiple
title: Метод Reset класса CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 05a10737eac27b4c06380cae37af3ad9b235123dafbddfc3069a42221706806b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701494"
---
# <a name="reset-method-of-the-cim_pcvideocontroller-class"></a>Метод Reset \_ класса CIM пквидеоконтроллер

Метод **Reset** \_ класса CIM пквидеоконтроллер запрашивает сброс логического устройства. Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.

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

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике. Классы WMI, производные от [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md), см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[\_ПКВИДЕОКОНТРОЛЛЕР CIM](reset-method-in-class-cim-pcvideocontroller.md)
</dt> <dt>

[**\_ПКВИДЕОКОНТРОЛЛЕР CIM**](cim-pcvideocontroller.md)
</dt> </dl>

 

 




