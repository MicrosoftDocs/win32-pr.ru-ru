---
description: Вызывается методом Цертделетектлфромсторе перед удалением списка доверия сертификатов из хранилища.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Функция обратного вызова Цертсторепровделетектл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908971"
---
# <a name="certstoreprovdeletectl-callback-function"></a>Функция обратного вызова Цертсторепровделетектл

Функция обратного вызова **цертсторепровделетектл** вызывается [**цертделетектлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) перед удалением списка доверия сертификатов из хранилища. Эта функция определяет, можно ли удалить список доверия сертификатов.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсторепров* \[ окне\]
</dt> <dd>

**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).

</dd> <dt>

*пктлконтекст* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Все необходимые значения флагов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если список доверия сертификатов можно удалить из хранилища.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



 

 
