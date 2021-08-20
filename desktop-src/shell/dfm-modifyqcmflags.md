---
description: 'Позволяет обратному вызову изменять \_ значения CFM XXX, переданные в IContextMenu:: куериконтекстмену.'
title: Сообщение DFM_MODIFYQCMFLAGS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62ce86426b31abfb6dec67d7ee45b01a8bc47ba10c40ce9ed00051dd414a0ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223594"
---
# <a name="dfm_modifyqcmflags-message"></a>\_Сообщение DFM модификкмфлагс

Позволяет обратному вызову изменять \_ значения CFM XXX, переданные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пуневфлагс* \[ окне\]
</dt> <dd>

Указатель на новые значения флагов.

</dd> <dt>

*уфлагс* \[ окне\]
</dt> <dd>

Флаги, указывающие, как можно изменить контекстное меню. Этот параметр использует значения КМФ \_ xxx, описанные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                             |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 




