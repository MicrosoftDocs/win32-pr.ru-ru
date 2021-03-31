---
title: Класс Win32_RDMSManagementData
description: Синхронизирует данные публикации для служб удаленный рабочий стол Management Services (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSManagementData службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSManagementData, описание
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071216"
---
# <a name="win32_rdmsmanagementdata-class"></a>\_Класс Win32 рдмсманажементдата

Синхронизирует данные публикации для служб удаленный рабочий стол Management Services (RDMS).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсманажементдата** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсманажементдата** содержит следующие методы.



| Метод                                                                                        | Описание                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**синчронизеаллпублишингдата**](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | Синхронизирует все данные публикации для RDMS.<br/>                  |
| [**синчронизепублишингдата**](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | Синхронизирует указанный набор публикуемых данных для RDMS.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик служб удаленный рабочий стол Management Services](rdms-api-reference.md)
</dt> </dl>

 

 





