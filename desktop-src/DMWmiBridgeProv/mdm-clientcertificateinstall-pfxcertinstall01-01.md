---
title: Класс MDM_ClientCertificateInstall_PFXCertInstall01_01
description: Класс MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01 позволяет Организации использовать уникальные идентификаторы для различения разных запросов на установку сертификатов.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- Класс MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136790"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a>\_Класс MDM клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01** позволяет Организации использовать уникальные идентификаторы для различения разных запросов на установку сертификатов.

Требуется для установки сертификата PFX. При вызове Delete на этом узле необходимо удалить сертификаты и ключи, которые были установлены соответствующим BLOB-объектом PFX.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01** имеет эти свойства.

<dl> <dt>

[ContainerName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
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

Определяет имя родительского узла. Для этого класса — уникальный идентификатор для различения разных запросов на установку сертификатов.

</dd> <dt>

[KeyLocation](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
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

Описывает полный путь к родительскому узлу.

Строка имеет значение "./вендор/мсфт/клиентцертификатеинсталл/пфксцертинсталл"

</dd> <dt>

[пфксцертблоб](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **октетстринг**
</dt> </dl>

</dd> <dt>

[пфксцертпассворд](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[пфксцертпассворденкриптионсторе](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[пфксцертпассворденкриптионтипе](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[пфкскэйекспортабле](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Состояние](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Отпечаток](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
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

 

