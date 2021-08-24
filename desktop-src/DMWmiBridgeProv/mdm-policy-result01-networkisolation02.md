---
title: Класс MDM_Policy_Result01_NetworkIsolation02
description: '\_Класс политики MDM \_ Result01 \_ NetworkIsolation02 представляет доступные политики браузера.'
ms.assetid: f44f43fb-813b-4d40-a56c-0c497e004a8a
keywords:
- Класс MDM_Policy_Result01_NetworkIsolation02
- MDM_Policy_Result01_NetworkIsolation02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_NetworkIsolation02
- MDM_Policy_Result01_NetworkIsolation02.InstanceID
- MDM_Policy_Result01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6906d7a7f8cf6ad140683aabfd5068097da4e96ded9dd961cd8d6e1ff4e819
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815754"
---
# <a name="mdm_policy_result01_networkisolation02-class"></a>\_Класс политики MDM \_ Result01 \_ NetworkIsolation02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **\_ политики MDM \_ Result01 \_ NetworkIsolation02** представляет доступные политики браузера.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
  string NeutralResources;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Result01 \_ NetworkIsolation02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Result01 \_ NetworkIsolation02** имеет следующие свойства.

<dl> <dt>

[ентерприсеклаудресаурцес](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсеинтерналпроксисерверс](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсеипранже](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсеипранжесареаусоритативе](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсенетворкдомаиннамес](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсепроксисерверс](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсепроксисерверсареаусоритативе](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Нетворкисолатион".

</dd> <dt>

[неутралресаурцес](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

