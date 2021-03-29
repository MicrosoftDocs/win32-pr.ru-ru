---
title: Класс MDM_EnterpriseModernAppManagement_AppManagement01
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 запускает центр обновления Windows Scan и сообщает о последней ошибке сканирования.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262202"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a>\_Класс MDM ентерприсемодернаппманажемент \_ AppManagement01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** запускает центр обновления Windows Scan и сообщает о последней ошибке сканирования.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** содержит следующие методы.



| Метод                                                                                               | Описание                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**ремовепаккажемесод**](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | Метод удаления пакетов.<br/>                |
| [**упдатесканмесод**](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | Метод для запуска сканирования Центр обновления Windows.<br/> |



 

### <a name="properties"></a>Свойства

Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** имеет следующие свойства.

<dl> <dt>

[аппинвенторикуери](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[аппинвенториресултс](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Аппманажемент".

</dd> <dt>

[ластсканеррор](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/"

</dd> <dt>

[RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
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

 

