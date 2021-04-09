---
title: Класс MDM_VPNv2_RouteList02_01
description: Класс MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01 содержит необязательный список маршрутов, которые будут добавлены в таблицу МАРШРУТИЗАЦИИ для интерфейса VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Класс MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071843"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>\_Класс MDM поддержка vpnv2 \_ RouteList02 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01** содержит необязательный список маршрутов, которые будут добавлены в таблицу маршрутизации для интерфейса VPN.

Это необходимо для случая разделенного туннелирования, когда сайт VPN-сервера имеет больше подсетей, подсеть по умолчанию на основе IP-адреса, назначенного интерфейсу.

Каждый компьютер, на котором работает TCP/IP, принимает решения о маршрутизации. Эти решения контролируются таблицей IP-маршрутизации. Добавление значений в этом узле обновляет таблицу маршрутизации с маршрутами для подключения к интерфейсу VPN POST. Значения в этом узле представляют префикс назначения для IP-маршрутов. Префикс назначения состоит из префикса IP-адреса и длины префикса.

Добавление маршрута позволяет сетевому стеку обнаруживать трафик, который должен пройти через VPN-интерфейс для разбиения VPN-подключения с разделением туннеля. Некоторые VPN-серверы могут настроить это во время согласования подключения, и эти сведения не нужны в профиле VPN. Обратитесь к администратору VPN-сервера, чтобы определить, требуются ли эти сведения в профиле VPN.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01** имеет эти свойства.

<dl> <dt>

[Адрес](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/раутелист"

</dd> <dt>

[префикссизе](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
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

 

