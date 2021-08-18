---
description: Функция Аусзжетцентралакцессполицикаллбакк — это определяемая приложением функция, которая получает централизованную политику доступа. Аусзжетцентралакцессполицикаллбакк — это заполнитель для имени определяемой приложением функции.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Функция обратного вызова Аусзжетцентралакцессполицикаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5e8fd0afbd901d48386859e9b5d3557a173cfe6a23d749dc776992a4aedebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783748"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Функция обратного вызова Аусзжетцентралакцессполицикаллбакк

Функция *аусзжетцентралакцессполицикаллбакк* — это определяемая приложением функция, которая получает централизованную политику доступа. *Аусзжетцентралакцессполицикаллбакк* — это заполнитель для имени определяемой приложением функции.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хаусзклиентконтекст* \[ окне\]
</dt> <dd>

Обработчик контекста клиента.

</dd> <dt>

*капид* \[ окне\]
</dt> <dd>

Идентификатор извлекаемой централизованной политики доступа.

</dd> <dt>

*паргс* \[ в необязательное\]
</dt> <dd>

Необязательные аргументы, которые были переданы функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) через элемент **оптионаларгументс** структуры [**\_ \_ запроса на доступ к авторизации**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .

</dd> <dt>

*пцентралакцессполициаппликабле* \[ заполняет\]
</dt> <dd>

Указатель на логическое значение, используемое диспетчером ресурсов, чтобы указать, следует ли использовать централизованную политику доступа во время оценки доступа.

</dd> <dt>

*ппцентралакцессполици* \[ заполняет\]
</dt> <dd>

Указатель на централизованную политику доступа (CAP), используемую для оценки доступа. Если это значение равно **null**, применяется ограничение по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, функция возвращает **значение true**.

Если функция не может выполнить вычисление, она возвращает **значение false**. Используйте [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , чтобы вернуть ошибку в функцию проверки доступа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                   |
| Распространяемые компоненты<br/>          | Windows пакет средств администрирования сервера 2003 в Windows XP<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_запрос на доступ к AUTHZ \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**\_ \_ сведения о инициализации AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

