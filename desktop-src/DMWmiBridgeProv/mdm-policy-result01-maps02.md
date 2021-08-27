---
title: Класс MDM_Policy_Result01_Maps02
description: '\_Класс политики MDM \_ Result01 \_ Maps02 представляет доступные политики отображения.'
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- Класс MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d0927149650b4da948983646e73772e1d19af4237ada01d1654f160629de75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109324"
---
# <a name="mdm_policy_result01_maps02-class"></a>\_Класс политики MDM \_ Result01 \_ Maps02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **\_ политики MDM \_ Result01 \_ Maps02** представляет доступные политики отображения.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Result01 \_ Maps02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Result01 \_ Maps02** имеет следующие свойства.

<dl> <dt>

[алловоффлинемапсдовнлоадоверметередконнектион](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[енаблеоффлинемапсаутаупдате](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
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

Определяет имя родительского узла. для этого класса строка имеет значение "Карты".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

