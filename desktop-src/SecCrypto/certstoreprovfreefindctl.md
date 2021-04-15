---
description: Вызывается, когда сертификат, возвращенный обратным вызовом Цертсторепровфиндктл, не использовался и, следовательно, освобождается при последующем вызове Цертсторепровфиндктл.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Функция обратного вызова Цертсторепровфрифиндктл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683293"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Функция обратного вызова Цертсторепровфрифиндктл

Функция обратного вызова **цертсторепровфрифиндктл** вызывается, когда сертификат, возвращенный обратным вызовом [**цертсторепровфиндктл**](certstoreprovfindctl.md) , не использовался и, следовательно, освобождается при последующем вызове **цертсторепровфиндктл**. Перед вызовом функции обратного вызова CLOSE все сертификаты, возвращаемые обратным вызовом [**цертсторепровфиндктл**](certstoreprovfindctl.md) , должны быть освобождены поставщиком с помощью **цертсторепровфиндктл** или **цертсторепровфрифиндктл**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
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

Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*пвсторепровфиндинфо* \[ окне\]
</dt> <dd>

Указатель на буфер, содержащий сведения о поиске.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Все необходимые значения флагов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**цертсторепровфиндктл**](certstoreprovfindctl.md)
</dt> <dt>

[**\_контекст CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
