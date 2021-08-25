---
description: Извлекает указанное свойство списка отзыва сертификатов.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Функция обратного вызова Цертсторепровжеткрлпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877054"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Функция обратного вызова Цертсторепровжеткрлпроперти

Функция обратного вызова **цертсторепровжеткрлпроперти** извлекает указанное свойство [*списка отзыва сертификатов*](../secgloss/c-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
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

*пкрлконтекст* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ контекста списка отзыва сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .

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

Указатель на буфер, содержащий указатель на структуру [**\_ контекста списка отзыва сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) , возвращаемую функцией. При первом вызове функции может быть задано значение **null** , чтобы получить значение *пкбдата* перед выделением памяти для буфера.

</dd> <dt>

*пкбдата* \[ в, out\]
</dt> <dd>

Указатель на **DWORD** , указывающий длину буфера *пвдата* .

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

[**Контекст списка отзыва сертификатов \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
