---
description: Выполняет перечисление или поиск первого или следующего списка доверия (CTL) во внешнем хранилище, соответствующем указанным критериям.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Функция обратного вызова Цертсторепровфиндктл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f3064b42961196a7522fba6d08ac684aa4421b26727cdf229854351c777a4b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770011"
---
# <a name="certstoreprovfindctl-callback-function"></a>Функция обратного вызова Цертсторепровфиндктл

Функция обратного вызова **цертсторепровфиндктл** перечисляет или находит первый или следующий [*список CTL*](../secgloss/c-gly.md) во [*внешнем хранилище*](../secgloss/e-gly.md) , соответствующий указанным критериям.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
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

Указатель на [**\_ хранилище сертификатов \_ Prov \_ найти \_ информационную**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) структуру, содержащую все параметры, переданные в [**цертфиндктлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore). .

</dd> <dt>

*ппревктлконтекст* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) для последнего найденного списка доверия. При первом вызове функции этот параметр должен иметь значение **null**. При последующих вызовах ему следует задать указатель, возвращенный в параметре *пппровктлконтекст* последнего вызова. Непустой указатель , переданный в этом параметре, освобождается функцией обратного вызова.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Все необходимые значения флагов.

</dd> <dt>

*ппвсторепровфиндинфо* \[ в, out\]
</dt> <dd>

Указатель на указатель на буфер для возврата сведений о поставщике хранилища. При необходимости обратный вызов может вернуть указатель на внутреннюю информацию поиска в этом параметре. После первого вызова этот параметр устанавливается в указатель, возвращенный предыдущим вызовом функции.

</dd> <dt>

*пппровктлконтекст* \[ заполняет\]
</dt> <dd>

При успешном обнаружении в этом параметре возвращается указатель на найденный список доверия.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ сведения о поиске Prov в хранилище сертификатов \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**цертфиндктлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**\_контекст CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
