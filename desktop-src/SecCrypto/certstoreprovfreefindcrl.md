---
description: Вызывается, когда сертификат, возвращенный обратным вызовом Цертсторепровфиндкрл, не использовался и, следовательно, освобождается при последующем вызове Цертсторепровфиндкрл.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Функция обратного вызова Цертсторепровфрифиндкрл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769939"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Функция обратного вызова Цертсторепровфрифиндкрл

Функция обратного вызова **цертсторепровфрифиндкрл** вызывается, когда сертификат, возвращенный обратным вызовом [**цертсторепровфиндкрл**](certstoreprovfindcrl.md) , не использовался и, следовательно, освобождается при последующем вызове **цертсторепровфиндкрл**. Перед вызовом функции обратного вызова CLOSE все сертификаты, возвращаемые обратным вызовом [**цертсторепровфиндкрл**](certstoreprovfindcrl.md) , должны быть освобождены поставщиком с помощью **цертсторепровфиндкрл** или **цертсторепровфрифиндкрл**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
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

*пкрлконтекст* \[ окне\]
</dt> <dd>

Указатель на [**\_ контекст списка отзыва сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**цертсторепровфиндкрл**](certstoreprovfindcrl.md)
</dt> <dt>

[**Контекст списка отзыва сертификатов \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
