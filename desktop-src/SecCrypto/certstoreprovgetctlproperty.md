---
description: Извлекает указанное свойство списка доверия сертификатов (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Функция обратного вызова Цертсторепровжетктлпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1677c2cccbdf0b422696437736380bd0bb57542220a898332d72ec7a0562fd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769763"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Функция обратного вызова Цертсторепровжетктлпроперти

Функция обратного вызова **цертсторепровжетктлпроперти** извлекает указанное свойство [*списка доверия сертификатов*](../secgloss/c-gly.md) (CTL).

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

**Хцертсторепровный** обработчик [*хранилища сертификатов*](../secgloss/c-gly.md).

</dd> <dt>

*пктлконтекст* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

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

Указатель на буфер, содержащий указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) , возвращаемую функцией. Чтобы получить значение *пкбдата* перед выделением памяти для буфера, этот параметр можно установить в **значение NULL** при первом вызове функции.

</dd> <dt>

*пкбдата* \[ в, out\]
</dt> <dd>

Указатель на **DWORD** , указывающий длину буфера *пвдата* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, функция возвращает ненулевое значение.

Если функция завершается ошибкой, она возвращает ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_контекст CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
