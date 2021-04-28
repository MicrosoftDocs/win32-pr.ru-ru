---
description: Метод РемовеассоЦиатеддата класса Msvm_CollectionReferencePointService — удаляет журнал данных, связанный с точкой ссылки.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Метод РемовеассоЦиатеддата класса Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66a5cf068545f31f9919a9da60a1b09b32f78e4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119232"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a>Метод РемовеассоЦиатеддата \_ класса Коллектионреференцепоинтсервице мсвм

Удаляет журнал данных, связанный с точкой ссылки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедреференцепоинтколлектион* \[ окне\]
</dt> <dd>

Ссылка на затронутую коллекцию опорных точек виртуальной системы.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ коллектионреференцепоинтсервице**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




