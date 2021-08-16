---
description: Перечисляет или находит первый или следующий сертификат во внешнем хранилище, соответствующий указанным критериям.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Функция обратного вызова Цертсторепровфиндцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770023"
---
# <a name="certstoreprovfindcert-callback-function"></a>Функция обратного вызова Цертсторепровфиндцерт

Функция обратного вызова **цертсторепровфиндцерт** перечисляет или находит первый или следующий сертификат во [*внешнем хранилище*](../secgloss/e-gly.md) , соответствующий указанным критериям.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсторепров* \[ окне\]
</dt> <dd>

**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).

</dd> <dt>

*пфиндинфо* \[ окне\]
</dt> <dd>

Указатель на [**\_ хранилище сертификатов \_ Prov \_ найти \_ информационную**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) структуру, содержащую все параметры, переданные в функцию [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .

</dd> <dt>

*ппревцертконтекст* \[ окне\]
</dt> <dd>

Указатель на [**\_ контекст**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) сертификата найденного сертификата. При первом вызове функции этот параметр должен иметь значение **null**. При последующих вызовах ему следует задать указатель, возвращенный в параметре *пппровцертконтекст* последнего вызова. Непустой указатель , переданный в этом параметре, освобождается функцией обратного вызова.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Все необходимые значения флагов.

</dd> <dt>

*ппвсторепровфиндинфо* \[ в, out\]
</dt> <dd>

Указатель на указатель на буфер для возврата сведений о поставщике хранилища. При необходимости обратный вызов может вернуть указатель на внутреннюю информацию поиска в этом параметре. После первого вызова этот параметр устанавливается в указатель, возвращенный предыдущим вызовом функции.

</dd> <dt>

*пппровцертконтекст* \[ заполняет\]
</dt> <dd>

При успешном обнаружении в этом параметре возвращается указатель на найденный сертификат.

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
</dt> <dt>

[**\_ \_ \_ сведения о поиске Prov в хранилище сертификатов \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
