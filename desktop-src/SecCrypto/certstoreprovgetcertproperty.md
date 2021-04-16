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
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662891"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
