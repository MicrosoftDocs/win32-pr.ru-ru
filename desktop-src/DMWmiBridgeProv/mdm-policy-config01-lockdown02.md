---
title: Класс MDM_Policy_Config01_LockDown02
description: '\_Класс политики MDM \_ Config01 \_ Lockdown02 представляет доступные политики блокировки.'
ms.assetid: 1d744400-70db-4f6b-97d0-7799fdfda44f
keywords:
- Класс MDM_Policy_Config01_LockDown02
- MDM_Policy_Config01_LockDown02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LockDown02
- MDM_Policy_Config01_LockDown02.InstanceID
- MDM_Policy_Config01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4794b085d5e2374756759055b6426ca3ca56c5562518e5a43715acd372d6c75c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527574"
---
# <a name="mdm_policy_config01_lockdown02-class"></a>\_Класс политики MDM \_ Config01 \_ LockDown02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **\_ политики MDM \_ Config01 \_ Lockdown02** представляет доступные политики блокировки.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Config01 \_ LockDown02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Config01 \_ LockDown02** имеет следующие свойства.

<dl> <dt>

[алловеджесвипе](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Lockdown".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

