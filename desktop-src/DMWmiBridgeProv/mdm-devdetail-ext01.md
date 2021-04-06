---
title: Класс MDM_DevDetail_Ext01
description: Класс MDM \_ DevDetail \_ Ext01 обрабатывает объект управления, который предоставляет параметры конкретного устройства для сервера OMA DM.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- Класс MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803125"
---
# <a name="mdm_devdetail_ext01-class"></a>\_Класс MDM DevDetail \_ Ext01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ DevDetail \_ Ext01** обрабатывает объект управления, который предоставляет параметры конкретного устройства для сервера OMA DM. Эти параметры устройства не отправляются с клиента на сервер автоматически, но их можно запрашивать с помощью команд OMA DM.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ DevDetail \_ Ext01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ DevDetail \_ Ext01** имеет следующие свойства.

<dl> <dt>

[девицехардваредата](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "ext"

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Девдетаил/"

</dd> <dt>

[вланмакаддресс](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
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

 

