---
title: Класс MDM_VPNv2_DomainNameInformationList02_01
description: Класс MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01 описывает правила таблица политики разрешения имен (NRPT) для профиля VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- Класс MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989219"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a>\_Класс MDM поддержка vpnv2 \_ DomainNameInformationList02 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01** описывает правила таблица политики разрешения имен (NRPT) для профиля VPN.

Таблица политики разрешения имен (NRPT) — это таблица пространств имен и соответствующие параметры, хранящиеся в реестре Windows, которые определяют поведение клиента DNS при выдаче запросов и обработке ответов. Каждая строка в таблице NRPT представляет правило для части пространства имен, для которого DNS-клиент выдает запросы. Перед выдачей запросов на разрешение имен DNS-клиент обращается к NRPT, чтобы определить, должны ли в запросе быть заданы дополнительные флаги. После получения ответа клиент снова обращается к NRPT для проверки каких либо специальных требований к обработке или политике. В отсутствие NRPT клиент работает на основе DNS-серверов и суффиксов, установленных для интерфейса.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01** имеет эти свойства.

<dl> <dt>

[DnsServers](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Имя_домена](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[домаиннаметипе](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
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

Определяет имя родительского узла.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"

</dd> <dt>

[вебпроксисерверс](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
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

 

