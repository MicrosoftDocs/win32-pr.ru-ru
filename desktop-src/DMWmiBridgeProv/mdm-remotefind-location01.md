---
title: Класс MDM_RemoteFind_Location01
description: Класс MDM \_ ремотефинд \_ Location01 извлекает сведения о расположении для конкретного устройства.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- Класс MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01 класс, описание
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36942badfe975a28d5212e502ab28984fa745f4a7563c39ed1cebb7d1b5dbcef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077028"
---
# <a name="mdm_remotefind_location01-class"></a>\_Класс MDM ремотефинд \_ Location01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ ремотефинд \_ Location01** извлекает сведения о расположении для конкретного устройства.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ремотефинд \_ Location01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ ремотефинд \_ Location01** имеет следующие свойства.

<dl> <dt>

[Точность](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Age](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Высота над уровнем моря](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[алтитудеаккураци](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
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

Определяет имя родительского узла. Для этого класса строка имеет значение Location.

</dd> <dt>

[Широта](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Долгота](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ремотефинд"

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

