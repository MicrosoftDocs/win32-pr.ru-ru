---
title: Класс Win32_RDAllowListFileAssociation
description: Описывает сопоставление типа опубликованного файла с удаленным приложением RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDAllowListFileAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDAllowListFileAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490590"
---
# <a name="win32_rdallowlistfileassociation-class"></a>\_Класс Win32 рдалловлистфилеассоЦиатион

Описывает сопоставление типа опубликованного файла с удаленным приложением RemoteApp.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдалловлистфилеассоЦиатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдалловлистфилеассоЦиатион** имеет следующие свойства.

<dl> <dt>

**аппалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Псевдоним удаленного приложения RemoteApp, связанного с расширением.

</dd> <dt>

**екстнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя расширения, например TXT.

</dd> <dt>

**прогидхинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указание для справки по открытию документов с этой ассоциацией файлов

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

 





