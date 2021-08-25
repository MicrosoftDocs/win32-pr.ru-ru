---
description: Метод Invoke \_ класса CIM меморичекк оценивает определенную проверку. Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными \_ подклассами проверки CIM. Этот метод наследуется от \_ проверки CIM.
ms.assetid: 264a7690-b066-4024-8cb1-d988b829dc72
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_MemoryCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1607d6b6db173b79db19584444b6928fc0e87b9ecf11e39b9e67e34acdb29496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003664"
---
# <a name="invoke-method-of-the-cim_memorycheck-class"></a>Метод Invoke \_ класса CIM меморичекк

Метод **Invoke** класса [**CIM \_ меморичекк**](cim-memorycheck.md) оценивает определенную проверку. Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными подклассами [**\_ проверки CIM**](cim-check.md) . Этот метод наследуется **от \_ проверки CIM**.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.

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

[\_МЕМОРИЧЕКК CIM](invoke-method-in-class-cim-memorycheck.md)
</dt> <dt>

[**\_МЕМОРИЧЕКК CIM**](cim-memorycheck.md)
</dt> </dl>

 

