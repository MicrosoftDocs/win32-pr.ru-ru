---
description: Вызывается, когда сертификат, возвращенный обратным вызовом Цертсторепровфиндцерт, не использовался и, следовательно, освобождается при последующем вызове Цертсторепровфиндцерт.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Функция обратного вызова Цертсторепровфрифиндцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664008"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Функция обратного вызова Цертсторепровфрифиндцерт

Функция обратного вызова **цертсторепровфрифиндцерт** вызывается, когда сертификат, возвращенный обратным вызовом [**цертсторепровфиндцерт**](certstoreprovfindcert.md) , не использовался и, следовательно, освобождается при последующем вызове **цертсторепровфиндцерт**. Перед вызовом функции обратного вызова CLOSE все сертификаты, возвращаемые обратным вызовом [**цертсторепровфиндцерт**](certstoreprovfindcert.md) , должны быть освобождены поставщиком с помощью **цертсторепровфиндцерт** или **цертсторепровфрифиндцерт**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
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

*пцертконтекст* \[ окне\]
</dt> <dd>

Указатель на [**\_ контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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

[**\_контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**цертсторепровфиндцерт**](certstoreprovfindcert.md)
</dt> </dl>

 

 
