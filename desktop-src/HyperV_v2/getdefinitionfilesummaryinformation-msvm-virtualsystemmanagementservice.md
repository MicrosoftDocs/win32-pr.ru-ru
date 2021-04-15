---
description: Возвращает сводные данные о виртуальной машине для указанных файлов определения виртуальной машины.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Метод Жетдефинитионфилесуммаринформатион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682798"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Жетдефинитионфилесуммаринформатион \_ класса Виртуалсистемманажементсервице мсвм

Возвращает сводные данные о виртуальной машине для указанных файлов определения виртуальной машины.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дефинитионфилес* \[ окне\]
</dt> <dd>

Массив путей к XML-файлам конфигурации, для которых возвращаются сводные данные.

</dd> <dt>

*SummaryInformation* \[ заполняет\]
</dt> <dd>

Массив экземпляров [**мсвм \_ суммаринформатионбасе**](msvm-summaryinformation.md) , содержащих запрашиваемые сведения для виртуальных машин и (или) моментальных снимков, указанных в массиве *дефинитионфилес* . Возвращаются только свойства **Name**, **ElementName**, **CreationTime** и **Notes** , все остальные свойства будут иметь **значение NULL**.

> [!Note]  

 

До Windows 10 версии 1703 тип данных был [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




