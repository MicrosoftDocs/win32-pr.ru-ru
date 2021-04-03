---
description: Запросите маркер для конечной точки службы, используя указанные учетные данные.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Метод Иупдатиндпоинтауспровидер:: Жетендпоинттокен (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810210"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>Метод Иупдатиндпоинтауспровидер:: Жетендпоинттокен

Запросите маркер для конечной точки службы, используя указанные учетные данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*serviceId* \[ окне\]
</dt> <dd>

Определяет обновляемую службу.

</dd> <dt>

*endpointType* \[ окне\]
</dt> <dd>

Определяет тип конечной точки, реализуемой службой.

</dd> <dt>

*проксисеттингс* \[ окне\]
</dt> <dd>

Параметры, используемые при соединении с прокси-сервером. Дополнительные сведения см. в разделе Структура [**упдатиндпоинтпроксисеттингс**](updateendpointproxysettings.md) .

</dd> <dt>

*хусертокен* \[ окне\]
</dt> <dd></dd> <dt>

*TokenType* \[ окне\]
</dt> <dd>

Определяет тип маркера проверки подлинности, используемый для проверки подлинности.

</dd> <dt>

*фрефрешонлине* \[ окне\]
</dt> <dd>

Указывает, что погода WUA запрашивает новый маркер. Значение true указывает, что запрашивается новый маркер. Значение false указывает, что запрошен новый или кэшированный токен. Дополнительные сведения см. в разделе "Примечания".

</dd> <dt>

*ппендпоинттокен* \[ заполняет\]
</dt> <dd>

Укажите токен конечной точки, который будет использоваться.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении возвращает значение ОК. В противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Комментарии

WUA обычно задает для параметра Фрефрешонлине значение false при первом вызове этого метода, а затем при возникновении ошибки подключения WUA устанавливает для параметра значение true при повторном вызове метода. Однако реализация этого метода может запросить новый маркер из службы маркеров безопасности (STS) или предоставить кэшированный маркер в любое время.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                   |
| Минимальная версия сервера<br/> | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                |
| Header<br/>                   | <dl> <dt>Упдатиндпоинтаус. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Упдатиндпоинтаус. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Упдатиндпоинтаус. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иупдатиндпоинтауспровидер**](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




