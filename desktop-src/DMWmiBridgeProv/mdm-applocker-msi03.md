---
title: Класс MDM_AppLocker_MSI03
description: Класс MDM \_ AppLocker \_ MSI03 определяет ограничения политики для обработки MSI файлов.
ms.assetid: b7b6602d-38b7-46f0-9542-71228ab0c303
keywords:
- Класс MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03.InstanceID
- MDM_AppLocker_MSI03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5bd17a979ac0e4a6dcbbc07a38ba72bfd50ede4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803826"
---
# <a name="mdm_applocker_msi03-class"></a>\_Класс MDM AppLocker \_ MSI03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ AppLocker \_ MSI03** определяет ограничения политики для обработки MSI файлов.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_MSI03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ AppLocker \_ MSI03** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ AppLocker \_ MSI03** имеет следующие свойства.

<dl> <dt>

[**енфорцементмоде**](/windows/client-management/mdm/applocker-csp)
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

Определяет имя родительского узла.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/аппликатионлаунчрестриктионс"

</dd> <dt>

[**Политика**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

 

