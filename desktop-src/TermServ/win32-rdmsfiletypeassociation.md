---
title: Класс Win32_RDMSFileTypeAssociation
description: Управляет сопоставлением типов файлов для опубликованного приложения.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSFileTypeAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSFileTypeAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414840"
---
# <a name="win32_rdmsfiletypeassociation-class"></a>\_Класс Win32 рдмсфилетипеассоЦиатион

Управляет сопоставлением типов файлов для опубликованного приложения.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсфилетипеассоЦиатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдмсфилетипеассоЦиатион** имеет следующие свойства.

<dl> <dt>

**аппалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает и задает псевдоним приложения, связанного с типом файла.

</dd> <dt>

**екстнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает имя расширения файла.

</dd> <dt>

**иконконтентс**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает содержимое значка для типа файла.

</dd> <dt>

**икониндекс**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает индекс значка для типа файла.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает путь к значку для типа файла.

</dd> <dt>

**испримарихандлер**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает значение, указывающее, относится ли сопоставление типа файла к основному обработчику. **Значение true** , если тип файла связан с основным обработчиком; в противном случае — **значение false**.

</dd> <dt>

**IsPublished**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Публикуется ли этот ФТА.

Возвращает и задает значение, указывающее, опубликована ли ассоциация типа файла. **Значение true** , если сопоставление типа файла Опубликовано; в противном случае — **значение false**.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает и задает имя пула приложений для сопоставления типа файла.

</dd> <dt>

**прогидхинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает указание, помогающее пользователям открыть расширение файла.

</dd> </dl>

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

 

