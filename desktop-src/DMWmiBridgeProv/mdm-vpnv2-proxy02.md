---
title: Класс MDM_VPNv2_Proxy02
description: Класс MDM \_ Поддержка vpnv2 \_ Proxy02 определяет объект конфигурации, обеспечивающий поддержку прокси-сервера после подключения для VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- Класс MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490659"
---
# <a name="mdm_vpnv2_proxy02-class"></a>\_Класс MDM поддержка vpnv2 \_ Proxy02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Поддержка vpnv2 \_ Proxy02** определяет объект конфигурации, обеспечивающий поддержку прокси-сервера после подключения для VPN. Прокси-сервер, определенный для этого профиля, применяется, если этот профиль активен и подключен.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Поддержка vpnv2 \_ Proxy02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Поддержка vpnv2 \_ Proxy02** имеет следующие свойства.

<dl> <dt>

[AutoConfigUrl](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
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

Определяет имя родительского узла. Коллекция объектов конфигурации, обеспечивающая поддержку прокси-сервера после подключения для VPN. Прокси-сервер, определенный для этого профиля, применяется, если этот профиль активен и подключен.

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

 

