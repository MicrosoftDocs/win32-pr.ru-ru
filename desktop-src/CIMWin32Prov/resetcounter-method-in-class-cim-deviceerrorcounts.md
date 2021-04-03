---
description: Метод Ресеткаунтер сбрасывает счетчики ошибок и предупреждений.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Метод Ресеткаунтер класса CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895474"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a>Метод Ресеткаунтер \_ класса CIM девицеерроркаунтс

Метод **ресеткаунтер** сбрасывает счетчики ошибок и предупреждений. Метод используется таким образом, чтобы инструментирование логического устройства, которое будет выводить ошибки и предупреждения в виде табуляции, также мог сбросить свою внутреннюю обработку и счетчики. В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе. Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Селектедкаунтер* \[ окне\]
</dt> <dd>

Счетчик ошибок для сброса.

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

**Все** (0)


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

**Счетчик неопределенных ошибок** (1)


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

**Счетчик критических ошибок** (2)


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

**Счетчик основных ошибок** (3)


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

**Счетчик незначительных ошибок** (4)


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

**Счетчик предупреждений** (5)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 (нуль) в случае успеха, 1 (один), если не поддерживается, и любое другое значение, если произошла ошибка.

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

[\_ДЕВИЦЕЕРРОРКАУНТС CIM](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[**\_ДЕВИЦЕЕРРОРКАУНТС CIM**](cim-deviceerrorcounts.md)
</dt> </dl>

 

