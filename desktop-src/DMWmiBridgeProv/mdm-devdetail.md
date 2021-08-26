---
title: Класс MDM_DevDetail
description: Класс MDM \_ DevDetail обрабатывает объект управления, который предоставляет параметры, относящиеся к устройству, к серверу OMA DM.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- Класс MDM_DevDetail
- MDM_DevDetail класс, описание
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cfed95a5ecb40408e45c3697be181270ee0deb16e54fac9aea4b45aa96faa4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053594"
---
# <a name="mdm_devdetail-class"></a>\_Класс MDM DevDetail

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ DevDetail** обрабатывает объект управления, который предоставляет параметры, относящиеся к устройству, к серверу OMA DM. Эти параметры устройства не отправляются с клиента на сервер автоматически, но их можно запрашивать с помощью команд OMA DM.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ DevDetail** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ DevDetail** имеет следующие свойства.

<dl> <dt>

[девтип](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[фвв](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[хвв](/windows/client-management/mdm/devdetail-csp#hwv)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "DevDetail".

</dd> <dt>

[лргобж](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[КАНАЛОВ](/windows/client-management/mdm/devdetail-csp#oem)
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

Описывает полный путь к родительскому узлу.

</dd> <dt>

[SwV](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

 

