---
title: Класс MDM_EnterpriseModernAppManagement_AppManagement01_02
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02 указывает, следует ли блокировать обновление определенного приложения с помощью автоматического обновления.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85aa9e5fc4dfc707dfbcf9c33831e71f0904f0b6c5db7498f9303beb40c9c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018182"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a>\_Класс MDM ентерприсемодернаппманажемент \_ AppManagement01 \_ 02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02** указывает, следует ли блокировать обновление определенного приложения с помощью автоматического обновления.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 02** имеет эти свойства.

<dl> <dt>

[донотупдате](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
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

Определяет имя родительского узла. Для этого класса строка является экземпляром имени семейства пакетов.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/аппманажемент/*EnterpriseID*"

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

