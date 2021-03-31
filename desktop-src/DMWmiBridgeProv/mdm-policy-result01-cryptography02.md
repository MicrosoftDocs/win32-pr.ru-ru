---
title: Класс MDM_Policy_Result01_Cryptography02
description: '\_Класс политики MDM \_ Result01 \_ Cryptography02 представляет политики, связанные с шифрованием.'
ms.assetid: 3ab41bb4-920d-4647-8f05-f6938f51c409
keywords:
- Класс MDM_Policy_Result01_Cryptography02
- MDM_Policy_Result01_Cryptography02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cryptography02
- MDM_Policy_Result01_Cryptography02.InstanceID
- MDM_Policy_Result01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6beb62d7d9fdba320220c9bb4de5074fce416ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136759"
---
# <a name="mdm_policy_result01_cryptography02-class"></a>\_Класс политики MDM \_ Result01 \_ Cryptography02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **\_ политики MDM \_ Result01 \_ Cryptography02** представляет политики, связанные с шифрованием.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Result01 \_ Cryptography02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ политики MDM \_ Result01 \_ Cryptography02** имеет следующие свойства.

<dl> <dt>

[AllowFipsAlgorithmPolicy](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Cryptography"

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

</dd> <dt>

[тлсЦиферсуитес](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
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

 

