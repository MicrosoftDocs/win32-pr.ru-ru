---
title: Класс MDM_Update_PendingRebootUpdates01_01
description: Класс MDM \_ Update \_ PendingRebootUpdates01 \_ 01 используется для управления обновлениями, ожидающими при перезагрузке.
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- Класс MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca640a4de00ea9eb115b999129a16dd0bf930cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137258"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a>\_Класс MDM обновления \_ PendingRebootUpdates01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** используется для управления обновлениями, ожидающими при перезагрузке.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** имеет эти свойства.

<dl> <dt>

[инсталледтиме](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Определяет имя родительского узла. Для этого класса строка представляет собой идентификатор GUID обновления, ожидающего перезагрузки.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/упдате/пендингребутупдатес"

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

