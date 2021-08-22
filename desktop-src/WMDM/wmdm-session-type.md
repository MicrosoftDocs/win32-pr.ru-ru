---
title: Перечисление WMDM_SESSION_TYPE
description: Тип \_ перечисления типа сеанса вмдм \_ определяет тип сеанса.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e3d3d774667ca0c7026caa05609efd69443e00c0c2e273a1e6ad0ac086aa9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055532"
---
# <a name="wmdm_session_type-enumeration"></a>\_ \_ Перечисление типов сеансов вмдм

Тип перечисления типа **\_ сеанса вмдм \_** определяет тип сеанса.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**ВМДМ \_ сеанс \_ нет**
</dt> <dd>

Сеанс не определен.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_Перенаправление сеанса вмдм \_ \_ на \_ устройство**
</dt> <dd>

Сеанс определяется как передача данных на устройство.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_Перемещение сеанса \_ вмдм \_ с \_ устройства**
</dt> <dd>

Сеанс определяется как передача данных с устройства.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_Удаление сеанса \_ вмдм**
</dt> <dd>

Сеанс определяется как удаление данных.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_пользовательский сеанс \_ вмдм**
</dt> <dd>

Сеанс определяется как пользовательский сеанс.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





