---
description: Уничтожает существующий моментальный снимок виртуальной машины.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Метод Дестройснапшот класса Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5ed582711b85fa51ceef6f5fb623a50089d80e0fb92e9eb12498efcd50840f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393385"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Метод Дестройснапшот \_ класса Виртуалсистемснапшотсервице мсвм

Уничтожает существующий моментальный снимок виртуальной машины. Этот метод может в качестве побочного результата уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедснапшот* \[ окне\]
</dt> <dd>

Ссылка на [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющая моментальный снимок виртуальной машины для уничтожения.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемснапшотсервице**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**Ремовевиртуалсистемснапшот (v1)**](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

