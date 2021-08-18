---
title: Структура WINBIO_ACCOUNT_POLICY (Винбио \_ Adapter. h)
description: Содержит политику антиподмены по умолчанию или учетную запись.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- API структуры WINBIO_ACCOUNT_POLICY биометрическая платформа Windows
- PWINBIO_ACCOUNT_POLICY API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c30241f0e13528c8427367c61362b803caaa9fc8c0a15a0eefad72689517d40f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035254"
---
# <a name="winbio_account_policy-structure"></a>\_Структура политики учетных записей винбио \_

Структура **\_ \_ политики учетных записей винбио** содержит политику антиподмены по умолчанию или учетную запись.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>Члены

<dl> <dt>

**Удостоверение**
</dt> <dd>

Структура [**\_ идентификации винбио**](winbio-identity.md) , указывающая сведения об учетной записи.

</dd> <dt>

**антиспуфбехавиор**
</dt> <dd>

Одно из значений [**перечисления \_ \_ \_ \_ действий политики антифишинга винбио**](winbio-anti-spoof-policy-action.md) , которое указывает действие политики подделки, которое будет использоваться для учетной записи.

</dd> </dl>

## <a name="remarks"></a>Remarks

Описание того, как используется эта структура, см. в обсуждении метода [**енгинеадаптерсетаккаунтполици**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                                     |
| Заголовок<br/>                   | <dl> <dt>Винбио \_ Adapter. h (включить винбио \_ Adapter. h)</dt> </dl> |



 

 





