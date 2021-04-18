---
title: Класс Win32_RDMSDeploymentSettings
description: Управляет параметрами развертывания для коллекции виртуальных рабочих столов.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSDeploymentSettings, описание
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534010"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>\_Класс Win32 рдмсдеплойментсеттингс

Управляет параметрами развертывания для коллекции виртуальных рабочих столов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсдеплойментсеттингс** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсдеплойментсеттингс** содержит следующие методы.



| Метод                                                                                                  | Описание                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**жетбасевхдпас**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.<br/>                 |
| [**ConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | Извлекает строку подключения к базе данных на уровне развертывания.<br/>                                                             |
| [**жетдиффвхдпас**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Возвращает путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.<br/>            |
| [**жетекспортпас**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | Извлекает путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.<br/>                  |
| [**GetInt32Property**](getint32property-win32-rdmsdeploymentsettings.md)                               | Извлекает целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.<br/>                             |
| [**жетсекондариконнектионстринг**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | Извлекает вторичную строку подключения базы данных уровня развертывания, которая может использоваться для поддержки истечения срока действия пароля.<br/> |
| [**жетсмбпас**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | Возвращает UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.<br/>      |
| [**жетстрингаррайдеплойментсеттинг**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Извлекает параметры развертывания для коллекции виртуальных рабочих столов.<br/>                                                    |
| [**жетстрингпроперти**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | Извлекает строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.<br/>                               |
| [**ремоведеплойментсеттинг**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | Удаляет параметры развертывания для коллекции виртуальных рабочих столов.<br/>                                                      |
| [**сетбасевхдпас**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.<br/>                 |
| [**сетконнектионстринг**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | Задает строку подключения к базе данных на уровне развертывания.<br/>                                                                  |
| [**сетдиффвхдпас**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Обновляет путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.<br/>              |
| [**сетекспортпас**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | Обновляет путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.<br/>                    |
| [**SetInt32Property**](setint32property-win32-rdmsdeploymentsettings.md)                               | Обновляет целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.<br/>                               |
| [**сетсекондариконнектионстринг**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | Задает вторичную строку подключения базы данных на уровне развертывания.<br/>                                                        |
| [**сетсмбпас**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | Обновляет UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.<br/>        |
| [**сетстрингаррайдеплойментсеттинг**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Обновляет параметры развертывания для коллекции виртуальных рабочих столов.<br/>                                                      |
| [**сетстрингпроперти**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | Обновляет строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.<br/>                                 |



 

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

 

 





