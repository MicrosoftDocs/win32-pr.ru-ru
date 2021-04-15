---
description: Создает точку ссылки для коллекции виртуальных систем.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Метод Креатереференцепоинт класса Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350315"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Метод Креатереференцепоинт \_ класса Коллектионреференцепоинтсервице мсвм

Создает точку ссылки для коллекции виртуальных систем.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коллекция* \[ окне\]
</dt> <dd>

Ссылка на затронутую коллекцию виртуальных систем.

</dd> <dt>

*Референцепоинтсеттингс* \[ окне\]
</dt> <dd>

Параметры параметров.

</dd> <dt>

*Референцепоинттипе* \[ окне\]
</dt> <dd>

Указывает тип контрольной точки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (1)


</dt> <dd>

Отслеживание журнала реплики Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (2)


</dt> <dd>

На основе устойчивых Отслеживание изменений виртуальных дисков.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl> </dd> <dt>

*Ресултингреференцепоинтколлектион* \[ в, out\]
</dt> <dd>

Результирующая эталонная точка коллекции виртуальных систем.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется долго, при необходимости может быть возвращено задание.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвращает 0 (без ошибок) или 4096 (задание запущено). в противном случае возвратите ошибку.

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ коллектионреференцепоинтсервице**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




