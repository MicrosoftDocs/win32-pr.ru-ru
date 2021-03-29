---
title: Класс Win32_RDCentralPublishedFileAssociation
description: Сведения о расширении файла, связанном с приложением.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDCentralPublishedFileAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDCentralPublishedFileAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492741"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a>\_Класс Win32 рдцентралпублишедфилеассоЦиатион

Сведения о расширении файла, связанном с приложением

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдцентралпублишедфилеассоЦиатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдцентралпублишедфилеассоЦиатион** имеет следующие свойства.

<dl> <dt>

**аппалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Псевдоним RemoteApp для сопоставления файлов.

</dd> <dt>

**екстнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя расширения (например, txt).

</dd> <dt>

**фармалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Псевдоним фермы Ремотеапп'с сопоставления файлов

</dd> <dt>

**иконконтентс**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Содержимое значка для этого сопоставления файлов.

</dd> <dt>

**примарихандлер**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Зарезервировано для последующего использования. Всегда будет иметь **значение true**.

</dd> <dt>

**прогидхинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указание, помогающее открывать документы с этой ассоциацией файлов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Тскпуб. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

