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
ms.openlocfilehash: 86a1cc421f4bd423137ff5699ebaf2412952e5f0f741952f91be15738b19b7ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109264"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a>\_Класс MDM обновления \_ PendingRebootUpdates01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

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

### <a name="properties"></a>Элемент Property

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
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

