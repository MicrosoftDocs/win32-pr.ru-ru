---
title: Класс MDM_VPNv2_NativeProfile02
description: Класс MDM \_ Поддержка vpnv2 \_ NativeProfile2 определяет сведения о профиле при использовании протокола VPN Windows Inbox (IKEV2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- Класс MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892517"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a>\_Класс MDM поддержка vpnv2 \_ NativeProfile02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Поддержка vpnv2 \_ NativeProfile2** определяет сведения о профиле при использовании протокола VPN Windows Inbox (IKEV2, PPTP, L2TP).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Поддержка vpnv2 \_ NativeProfile02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Поддержка vpnv2 \_ NativeProfile02** имеет следующие свойства.

<dl> <dt>

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

[L2tpPsk](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[NativeProtocolType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"

</dd> <dt>

[RoutingPolicyType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Серверы](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
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

 

