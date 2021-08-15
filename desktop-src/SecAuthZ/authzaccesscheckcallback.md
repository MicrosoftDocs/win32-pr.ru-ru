---
description: Определяемая приложением функция, которая обрабатывает записи контроля доступа (ACE) обратного вызова во время проверки доступа.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Функция обратного вызова Аусзакцессчекккаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5079b740d268174715b6c944787bb687cd9b8b1ecb12a27c04eeb26c79811034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784160"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Функция обратного вызова Аусзакцессчекккаллбакк

Функция **аусзакцессчекккаллбакк** — это определяемая приложением функция, которая обрабатывает [*записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) обратного вызова во время проверки доступа. **Аусзакцессчекккаллбакк** — это заполнитель для имени определяемой приложением функции. Приложение регистрирует этот обратный вызов, вызвав [**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хаусзклиентконтекст* \[ окне\]
</dt> <dd>

Маркер контекста клиента.

</dd> <dt>

*скорость* \[ окне\]
</dt> <dd>

Указатель на запись ACE для проверки включения в вызов функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

</dd> <dt>

*паргс* \[ в необязательное\]
</dt> <dd>

Данные, передаваемые в параметре *динамикграупаргс* вызова [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) или [**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).

</dd> <dt>

*пбацеаппликабле* \[ в, out\]
</dt> <dd>

Указатель на логическую переменную, которая получает результаты вычисления логики, определенной приложением.

Результаты имеют **значение true** , если логика определяет, что элемент ACE применим и будет включен в вызов [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); в противном случае результат будет **ложным**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, функция возвращает **значение true**.

Если функция не может выполнить вычисление, она возвращает **значение false**. Используйте [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , чтобы вернуть ошибку в функцию проверки доступа.

## <a name="remarks"></a>Remarks

Переменные атрибутов безопасности должны присутствовать в контексте клиента, если они ссылаются на условное выражение, в противном случае термин условного выражения, ссылающийся на них, будет считаться неизвестным.

Дополнительные сведения см. в статьях [как работают методы AccessCheck](how-dacls-control-access-to-an-object.md) и [централизованные политики авторизации](centralized-authorization-policy.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                   |
| Распространяемые компоненты<br/>          | Windows пакет средств администрирования сервера 2003 в Windows XP<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основные функции контроля доступа](authorization-functions.md)
</dt> <dt>

[Централизованная политика авторизации](centralized-authorization-policy.md)
</dt> <dt>

[Как работает AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**аусзинитиализеремотересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

