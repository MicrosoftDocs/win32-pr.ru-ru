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
ms.openlocfilehash: 5f3f6d224ed19073408015b3b83b90a66e9402d9b838d50eb7a8381e312e0534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877144"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**цертсторепровфиндктл**](certstoreprovfindctl.md)
</dt> <dt>

[**\_контекст CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
