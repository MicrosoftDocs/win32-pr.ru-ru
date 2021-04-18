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
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538345"
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

Тип узла — сервер сценариев Windows.

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_идентификатор узла \_ POWERSHELL**
</dt> <dd>

Тип узла — Windows PowerShell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_идентификатор узла \_ IE**
</dt> <dd>

Тип узла — Internet Explorer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_идентификатор узла \_ MSI**
</dt> <dd>

Тип узла — установщик Windows Майкрософт.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_ \_ максимальный идентификатор узла** 
</dt> <dd>

Максимальное значение перечисления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




