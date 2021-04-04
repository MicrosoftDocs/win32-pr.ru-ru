---
title: Класс MDM_Update_ApprovedUpdates01_01
description: Класс MDM \_ Update \_ ApprovedUpdates01 \_ 01 используется для управления развертыванием утвержденных обновлений.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- Класс MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988223"
---
# <a name="mdm_update_approvedupdates01_01-class"></a>\_Класс MDM обновления \_ ApprovedUpdates01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Update \_ ApprovedUpdates01 \_ 01** используется для управления развертыванием утвержденных обновлений.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Update \_ ApprovedUpdates01 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Update \_ ApprovedUpdates01 \_ 01** имеет эти свойства.

<dl> <dt>

[аппроведтиме](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
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

Определяет имя родительского узла. Для этого класса строка является идентификатором GUID утвержденного обновления.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/упдате/аппроведупдатес"

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

