---
description: Содержит параметры конфигурации EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Структура EAPOL_INTF_PARAMS (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663569"
---
# <a name="eapol_intf_params-structure"></a>\_ \_ Структура params EAPOL intf

\[**EAPOL \_ \_Параметры intf** больше не поддерживаются в Windows Vista и windows Server 2008. Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности. Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]

Содержит параметры конфигурации EAPOL.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Версия вызывающего объекта. Значение по умолчанию — 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**двеапфлагс**
</dt> <dd>

Не используется.

</dd> <dt>

**двеаптипе**
</dt> <dd>

Используемый тип расширения EAP. Задайте значение 0x00000013 для EAP-TLS и 0x00000026 для PEAP.

</dd> <dt>

**двсизеофссид**
</dt> <dd>

Размер идентификатора сети.

</dd> <dt>

**bSSID**
</dt> <dd>

Идентификатор сети.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Файл заголовка взксапи. h недоступен в Windows SDK.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 3 (SP3)<br/>                                                       |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Взксапи. h</dt> </dl> |



 

 




