---
title: Класс Win32_RDFileAssociation
description: Представляет сопоставление типов файлов для RemoteApp.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDFileAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDFileAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988518"
---
# <a name="win32_rdfileassociation-class"></a>\_Класс Win32 рдфилеассоЦиатион

Представляет сопоставление типов файлов для RemoteApp.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдфилеассоЦиатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдфилеассоЦиатион** имеет следующие свойства.

<dl> <dt>

**екстнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя расширения имени файла, например TXT.

</dd> <dt>

**иконконтентс**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Содержимое значка для этого сопоставления файлов.

</dd> <dt>

**икониндекс**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Индекс значка в файле.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к файлу значка для этого сопоставления файлов.

</dd> <dt>

**примарихандлер**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, относится ли эта ассоциация к основному обработчику.

</dd> <dt>

**прогидхинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указание, помогающее открывать документы с этой ассоциацией файлов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

 





