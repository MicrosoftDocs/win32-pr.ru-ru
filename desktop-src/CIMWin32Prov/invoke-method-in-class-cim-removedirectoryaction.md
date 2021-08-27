---
description: Метод Invoke \_ класса CIM ремоведиректоряктион принимает определенное действие. Сведения о том, как метод выполняет действие, зависит от реализации. Этот метод наследуется от \_ действия CIM.
ms.assetid: c6a7edcd-aac1-4364-8de5-a16fe2bab107
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_RemoveDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fab386bc41458ae4f4dd4593141af7671240a7f386c3fd9dfbb6c0d511071094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064874"
---
# <a name="invoke-method-of-the-cim_removedirectoryaction-class"></a>Метод Invoke \_ класса CIM ремоведиректоряктион

Метод **Invoke** класса [**CIM \_ ремоведиректоряктион**](cim-removedirectoryaction.md) принимает определенное действие. Сведения о том, как метод выполняет действие, зависит от реализации. Этот метод наследуется [**от \_ действия CIM**](cim-action.md).

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

[\_РЕМОВЕДИРЕКТОРЯКТИОН CIM](invoke-method-in-class-cim-removedirectoryaction.md)
</dt> <dt>

[**\_РЕМОВЕДИРЕКТОРЯКТИОН CIM**](cim-removedirectoryaction.md)
</dt> </dl>

 

