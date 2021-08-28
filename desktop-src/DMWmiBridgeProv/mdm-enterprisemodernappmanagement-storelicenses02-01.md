---
title: Класс MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Класс MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01 используется для управления лицензиями для приложений Магазина.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- Класс MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0342acc9cb74825552a409d686e5bc55f0cebc75642d5981a7144f3bac74bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018112"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a>\_Класс MDM ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** используется для управления лицензиями для приложений Магазина.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** содержит следующие методы.



| Метод                                                                                                              | Описание                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**аддлиценсемесод**](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | Метод добавления лицензии.<br/>                 |
| [**жетлиценсефромсторемесод**](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | Метод получения лицензии из магазина.<br/> |



 

### <a name="properties"></a>Свойства

Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** имеет эти свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Необязательный узел. Идентификатор лицензии для хранилища установленного приложения. Идентификатор лицензии обычно является PFNом приложения.

Поддерживаются операции добавления, получения и удаления.

</dd> <dt>

[лиценсекатегори](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[лиценсеусаже](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/апплиценсес/сторелиценсес"

</dd> <dt>

[рекуестерид](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
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

 

