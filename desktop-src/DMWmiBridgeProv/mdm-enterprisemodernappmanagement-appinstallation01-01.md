---
title: Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: класс MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01 используется для установки приложений из хранилища Windows или из размещенного расположения.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29cde4408cac13471e98d0c42b36779f8b23c0101f6ba22f383d97e181893e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875344"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>\_Класс MDM ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** используется для установки приложений из хранилища Windows или из размещенного расположения.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** содержит следующие методы.



| Метод                                                                                                    | Описание                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**хостединсталлмесод**](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | Метод для выполнения установки пакета приложения из размещенного расположения (это может быть локальный диск, UNC-источник данных или HTTPS).<br/> |
| [**стореинсталлмесод**](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | метод для выполнения установки приложения и лицензии из хранилища Windows.<br/>                                                    |



 

### <a name="properties"></a>Свойства

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** имеет эти свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Определяет имя родительского узла. Для этого класса строка имеет значение "Аппинсталлатион".

</dd> <dt>

[LastError](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ластеррордеск](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/аппинсталлатион"

</dd> <dt>

[прогрессстатус](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Состояние](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
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

 

