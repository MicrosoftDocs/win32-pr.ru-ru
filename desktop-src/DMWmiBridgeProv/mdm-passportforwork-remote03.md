---
title: Класс MDM_PassportForWork_Remote03
description: класс MDM \_ пасспортфорворк \_ Remote03 определяет Windows Hello для параметров удаленной политики для бизнеса.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- Класс MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3385a8bc2dee36bdfaa0707778ec0b1b40e0def22e9baea42eba2534c00b6be3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104284"
---
# <a name="mdm_passportforwork_remote03-class"></a>\_Класс MDM пасспортфорворк \_ Remote03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

класс **MDM \_ пасспортфорворк \_ Remote03** определяет Windows Hello для параметров удаленной политики для бизнеса.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ пасспортфорворк \_ Remote03** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ пасспортфорворк \_ Remote03** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

внутренний узел для определения удаленного Windows Hello для бизнес-политик. этот узел был добавлен в Windows 10 версии 1511.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

узел для определения параметров политики Windows Hello для бизнеса.

</dd> <dt>

[UseRemotePassport](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

