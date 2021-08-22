---
description: Создает опорную точку виртуальной системы.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Метод Креатереференцепоинт класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fdcf4680ff10bdc8135fae4ec3bb9f81d53c26092e7196e73965ee4f4d87991f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014482"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Метод Креатереференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм

Создает опорную точку виртуальной системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедсистем* \[ окне\]
</dt> <dd>

Объект [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , который ссылается на затронутую виртуальную систему.

</dd> <dt>

*Референцепоинтсеттингс* \[ окне\]
</dt> <dd>

Содержит настройки параметров.

</dd> <dt>

*Референцепоинттипе* \[ окне\]
</dt> <dd>

Тип запрошенной точки ссылки:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (0)


</dt> <dd>

На основе отслеживания журнала реплики Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (1)


</dt> <dd>

На основе устойчивых Отслеживание изменений виртуальных дисков.

</dd> </dl> </dd> <dt>

*Ресултингреференцепоинт* \[ в, out\]
</dt> <dd>

Результирующая эталонная точка виртуальной системы

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется долго, при необходимости может быть возвращено задание. В этом случае экземпляр класса [**мсвм \_ виртуалсистемреференцепоинт**](msvm-virtualsystemreferencepoint.md) , представляющий новую опорную точку виртуальной системы, представлен через ассоциацию [**CIM \_ аффектеджобелемент**](cim-affectedjobelement.md) со значением свойства **аффектеделемент** , ссылающегося на новый экземпляр класса **мсвм \_ виртуалсистемреференцепоинт** , который представляет точку ссылки на виртуальную систему, а значение **ElementEffects** установлено в 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает 0; в противном случае возвращает ошибку.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Недопустимый тип** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ виртуалсистемреференцепоинтсервице**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




