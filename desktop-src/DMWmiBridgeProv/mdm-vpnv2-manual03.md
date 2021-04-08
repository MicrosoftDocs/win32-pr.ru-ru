---
title: Класс MDM_VPNv2_Manual03
description: MDM \_ Поддержка vpnv2 \_ Manual03class — это необязательный узел, содержащий параметры ручного сервера.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- Класс MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989218"
---
# <a name="mdm_vpnv2_manual03-class"></a>\_Класс MDM поддержка vpnv2 \_ Manual03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Поддержка vpnv2 \_ Manual03** является дополнительным узлом, содержащим параметры ручного сервера.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ Поддержка vpnv2 \_ Manual03** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ Поддержка vpnv2 \_ Manual03** имеет следующие свойства.

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

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/прокси/"

</dd> <dt>

[Server](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
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

 

