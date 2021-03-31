---
title: Класс MSAD_DomainController
description: Представляет контроллер домена (DC), на котором работает поставщик WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- Класс MSAD_DomainController Active Directory
- Active Directory класса MSAD_DomainController, описание
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490740"
---
# <a name="msad_domaincontroller-class"></a>Класс МСАДного \_ класса (DomainController)

Представляет контроллер домена (DC), на котором работает поставщик WMI.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>Члены

Класс **\_ DomainController МСАД** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ DomainController МСАД** содержит следующие методы.



| Метод                                                 | Описание                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ексекутеккк**](executekcc-msad-domaincontroller.md) | Вызывает средство проверки согласованности знаний для проверки топологии репликации.<br/> |



 

### <a name="properties"></a>Свойства

Класс **\_ DomainController МСАД** имеет следующие свойства.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает общее имя объекта сервера.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает путь X. 500 объекта [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .

</dd> <dt>

**исадвертисингтолокатор**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, правильно ли объявлена служба локатора на контроллере домена. **Значение true** , если служба локатора на КОНТРОЛЛЕРе домена объявляется правильно; в противном случае — **значение false**.

</dd> <dt>

**исгк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, является ли контроллер домена сервером глобального каталога. **Значение true** , если контроллер домена является сервером глобального каталога; в противном случае — **значение false**.

</dd> <dt>

**иснекстридпулаваилабле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, получил ли контроллер домена другой пул RID. **Значение true** , если контроллер домена получил другой пул RID и выделение идентификаторов RID на этом контроллере домена может продолжаться даже в том случае, если текущий пул идентификаторов RID исчерпан. в противном случае — **значение false**.

</dd> <dt>

**исрегистерединднс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, правильно ли зарегистрирован контроллер домена в DNS. **Значение true** , если контроллер домена правильно зарегистрирован в DNS; в противном случае — **значение false**.

</dd> <dt>

**иссисволреади**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение, указывающее, правильно ли Опубликовано SysVol. **Значение true** , если SYSVOL опубликован правильно; в противном случае — **значение false**.

</dd> <dt>

**нтдсагуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает идентификатор GUID, связанный с объектом [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) в контейнере конфигурации. Объект **NTDS-DSA** представляет процесс домен Active Directory службы DSA на сервере.

</dd> <dt>

**перцентофридслефт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает процент идентификаторов RID, оставшихся в текущем пуле RID на этом контроллере домена.

</dd> <dt>

**Значением**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает сайт, на котором существует контроллер домена.

</dd> <dt>

**тимеофолдестрепладд**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Получает метку времени самой старой операции добавления репликации, которая все еще находится в очереди на этом контроллере домена.

</dd> <dt>

**тимеофолдестреплдел**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Получает метку времени самой старой операции удаления репликации, которая все еще находится в очереди на этом контроллере домена.

</dd> <dt>

**тимеофолдестреплмод**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Получает метку времени самой старой операции изменения репликации, которая все еще находится в очереди на этом контроллере домена.

</dd> <dt>

**тимеофолдестреплсинк**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Получает метку времени самой старой операции синхронизации репликации, которая все еще находится в очереди на этом контроллере домена.

</dd> <dt>

**тимеофолдестреплупдрефс**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Получает метку времени самой старой операции обновления репликации, которая все еще находится в очереди на этом контроллере домена.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

