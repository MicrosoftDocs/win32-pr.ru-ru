---
title: Класс Win32_RDMSEnvironment
description: Управляет средой служб управления удаленный рабочий стол (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSEnvironment, описание
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672616"
---
# <a name="win32_rdmsenvironment-class"></a>\_Класс Win32 рдмсенвиронмент

Управляет средой служб управления удаленный рабочий стол (RDMS).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсенвиронмент** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсенвиронмент** содержит следующие методы.



| Метод                                                                   | Описание                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**жетактивесервер**](getactiveserver-win32-rdmsenvironment.md)         | Возвращает полное доменное имя среды RDMS.<br/>                 |
| [**жетклиентакцесснаме**](getclientaccessname-win32-rdmsenvironment.md) | Извлекает имя записи ресурса системы доменных имен (DNS) для среды RDMS.<br/> |
| [**сетактивесервер**](setactiveserver-win32-rdmsenvironment.md)         | Задает полное доменное имя среды RDMS для текущего узла.<br/>                                |
| [**сетклиентакцесснаме**](setclientaccessname-win32-rdmsenvironment.md) | Обновляет имя RR DNS среды RDMS.<br/>                                          |



 

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

 

 





