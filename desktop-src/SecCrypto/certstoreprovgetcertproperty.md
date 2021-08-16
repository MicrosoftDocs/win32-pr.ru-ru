---
description: Извлекает указанное свойство сертификата.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Функция обратного вызова Цертсторепровжетцертпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c7d338c94c4e9655c125b0f70e3f2e8dfa732316a970c74c26e4a7fbced22671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769929"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Функция обратного вызова Цертсторепровжетцертпроперти

Функция обратного вызова **цертсторепровжетцертпроперти** извлекает указанное свойство сертификата.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
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

Указатель на структуру [**\_ контекста сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*dwPropId* \[ окне\]
</dt> <dd>

Указывает идентификатор свойства.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Все необходимые значения флагов.

</dd> <dt>

*пвдата* \[ заполняет\]
</dt> <dd>

Указатель на буфер, содержащий указатель на структуру [**\_ контекста сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) , возвращаемую функцией. При первом вызове функции может быть задано значение **null** , чтобы получить значение *пкбдата* перед выделением памяти для буфера.

</dd> <dt>

*пкбдата* \[ в, out\]
</dt> <dd>

Указатель на **DWORD** , указывающий длину буфера *пвдата* .

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

[**\_контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
