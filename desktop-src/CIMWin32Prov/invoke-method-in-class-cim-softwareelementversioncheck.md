---
description: Метод Invoke \_ класса CIM софтварилементверсиончекк оценивает определенную проверку.
ms.assetid: 5b477945-7ad4-49e2-b9c8-4a700a45f2b6
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_SoftwareElementVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d65921a07dd6e5ab6df54ea1ba71117c58a18dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538687"
---
# <a name="invoke-method-of-the-cim_softwareelementversioncheck-class"></a>Метод Invoke \_ класса CIM софтварилементверсиончекк

Метод **Invoke** класса [**CIM \_ софтварилементверсиончекк**](cim-softwareelementversioncheck.md) оценивает определенную проверку. Сведения о том, как метод оценивает определенную проверку в контексте CIM, описывается неабстрактными подклассами [**\_ проверки CIM**](cim-check.md) . Этот метод наследуется **от \_ проверки CIM**.

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

[\_СОФТВАРИЛЕМЕНТВЕРСИОНЧЕКК CIM](invoke-method-in-class-cim-softwareelementversioncheck.md)
</dt> <dt>

[**\_СОФТВАРИЛЕМЕНТВЕРСИОНЧЕКК CIM**](cim-softwareelementversioncheck.md)
</dt> </dl>

 

