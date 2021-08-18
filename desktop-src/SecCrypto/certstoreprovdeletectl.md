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
ms.openlocfilehash: befc031c1be441ad23c7a50563030775b625b81b66a9e1f92df4fb7c641fe73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993094"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



 

 
