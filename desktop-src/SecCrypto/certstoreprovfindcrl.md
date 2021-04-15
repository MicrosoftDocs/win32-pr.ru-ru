---
description: Выполняет перечисление или поиск первого или следующего списка CRL во внешнем хранилище, удовлетворяющем заданным условиям.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Функция обратного вызова Цертсторепровфиндкрл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546306"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Функция обратного вызова Цертсторепровфиндкрл

Функция обратного вызова **цертсторепровфиндкрл** перечисляет или находит первый или следующий [*список CRL*](../secgloss/c-gly.md) во внешнем [*хранилище*](../secgloss/e-gly.md) , соответствующее указанным критериям.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
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

Указатель на [**\_ хранилище сертификатов \_ Prov \_ найти \_ информационную**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) структуру, содержащую все параметры, переданные в функцию [**цертфиндкрлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .

</dd> <dt>

*ппревкрлконтекст* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ контекста CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) последнего найденного списка отзыва сертификатов. При первом вызове функции этот параметр должен иметь значение **null**. При последующих вызовах ему следует задать указатель, возвращенный в параметре *пппровкрлконтекст* последнего вызова. Непустой указатель , переданный в этом параметре, освобождается функцией обратного вызова.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Все необходимые значения флагов.

</dd> <dt>

*ппвсторепровфиндинфо* \[ в, out\]
</dt> <dd>

Указатель на указатель на буфер для возврата сведений о поставщике хранилища. При необходимости обратный вызов может вернуть указатель на внутреннюю информацию поиска в этом параметре. После первого вызова этот параметр устанавливается в указатель, возвращенный предыдущим вызовом функции.

</dd> <dt>

*пппровкрлконтекст* \[ заполняет\]
</dt> <dd>

При успешном обнаружении в этом параметре возвращается указатель на найденный список отзыва сертификатов.

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

[**\_ \_ \_ сведения о поиске Prov в хранилище сертификатов \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**цертфиндкрлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**Контекст списка отзыва сертификатов \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
