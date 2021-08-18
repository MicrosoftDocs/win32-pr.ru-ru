---
description: Определяет тип узла для вызывающего WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Перечисление WLDP_HOST_ID (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: fa52bc6259c75d5bb0929cb25610beb2b143515e2874b09bf04c454397a909e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758384"
---
# <a name="wldp_host_id-enumeration"></a>\_ \_ Перечисление идентификаторов узлов WLDP

Определяет тип узла для вызывающего WLDP.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ \_неизвестный \_ идентификатор узла** 
</dt> <dd>

Неизвестный тип узла.

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ \_ \_ глобальный идентификатор узла**
</dt> <dd>

Тип узла — Глобальная политика.

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**\_код узла \_ WLDP \_ VBA**
</dt> <dd>

Тип узла — VBScript.

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ \_идентификатор узла \_ WSH**
</dt> <dd>

тип узла — Windows сервер скриптов.

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_идентификатор узла \_ POWERSHELL**
</dt> <dd>

тип узла — Windows Powershell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_идентификатор узла \_ IE**
</dt> <dd>

Тип узла — Internet Explorer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_идентификатор узла \_ MSI**
</dt> <dd>

тип узла — установщик Windows майкрософт.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_ \_ максимальный идентификатор узла** 
</dt> <dd>

Максимальное значение перечисления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




