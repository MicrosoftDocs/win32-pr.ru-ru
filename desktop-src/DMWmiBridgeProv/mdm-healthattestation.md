---
title: Класс MDM_HealthAttestation
description: Класс MDM \_ хеалсаттестатион позволяет ИТ директорам предприятия оценивать работоспособность управляемых устройств и выполнять действия политики предприятия.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- Класс MDM_HealthAttestation
- MDM_HealthAttestation класс, описание
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489933"
---
# <a name="mdm_healthattestation-class"></a>\_Класс MDM хеалсаттестатион

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ ХЕАЛСАТТЕСТАТИОН** позволяет ИТ директорам предприятия оценивать работоспособность управляемых устройств и выполнять действия политики предприятия.

Ниже приведен список функций, выполняемых CSP Хеалсаттестатион.

-   Собирает данные, используемые для проверки состояния работоспособности устройств
-   передача данных службе аттестации работоспособности;
-   Подготавливает сертификат аттестации работоспособности, который он получает от,
-   После запроса перенаправляет сертификат аттестации работоспособности (полученный от) и связанные с ним сведения о среде выполнения на сервер MDM для проверки.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ хеалсаттестатион** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **MDM \_ хеалсаттестатион** содержит следующие методы.



| Метод                                                                 | Описание                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**верифихеалсмесод**](mdm-healthattestation-verifyhealthmethod.md) | Способ уведомления устройства о подготовке запроса на проверку сертификата работоспособности.<br/> |



 

### <a name="properties"></a>Свойства

Класс **MDM \_ хеалсаттестатион** имеет следующие свойства.

<dl> <dt>

[Сертификат](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **октетстринг**
</dt> </dl>

</dd> <dt>

[CorrelationID](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**куррентпротоколверсион**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

TBD

</dd> <dt>

[форцеретриеве](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[хасендпоинт](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Хеалсаттестатион".

</dd> <dt>

**макссуппортедпротоколверсион**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

TBD

</dd> <dt>

[Требуем](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/"

</dd> <dt>

**преферредмакспротоколверсион**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

TBD

</dd> <dt>

[Состояние](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[тпмреадистатус](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

