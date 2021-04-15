---
description: Запрашивает конечную точку, используемую для подключения к службе.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Метод Иупдатиндпоинтпровидер:: Жетсервицеендпоинт (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682762"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>Метод Иупдатиндпоинтпровидер:: Жетсервицеендпоинт

Запрашивает конечную точку, используемую для подключения к службе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ServiceId* \[ окне\]
</dt> <dd>

Определяет обновляемую службу.

</dd> <dt>

*endpointType* \[ окне\]
</dt> <dd>

Определяет тип конечной точки, реализуемой службой.

Перечисление [**упдатиндпоинттипе**](updateendpointtype.md) определяет следующие константы.

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**уетклиентсервер**


</dt> <dd>

Конечная точка клиент-сервер, которая используется для подключения к службе обновления.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**уетрепортинг**


</dt> <dd>

Конечная точка отчетов, используемая, когда клиент сообщает о результатах проверок, скачивается и устанавливается обратно в службу обновления.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**уетвуаселфупдате**


</dt> <dd>

Self-Updateая конечная точка, используемая, когда клиентский компьютер обращается к службе обновления, чтобы узнать, существует ли новая версия клиентского программного обеспечения агента Центр обновления Windows.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**уетрегулатион**


</dt> <dd>

Регулируемая конечная точка, используемая, когда клиентский компьютер обращается к регламентированной службе для работы с определенным обновлением, применимым к целевому компьютеру.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**уетсимплетаржетинг**


</dt> <dd>

Simple-Targeting ендоинт, используемый только с частными службами (WSUS-серверы в корпоративных средах).

</dd> </dl> </dd> <dt>

*проксисеттингс* \[ окне\]
</dt> <dd>

Определяет параметры, используемые при соединении с прокси-сервером.

</dd> <dt>

*хусертокен* \[ окне\]
</dt> <dd>

Содержит объект обработчика маркера, который представляет пользователя. Поставщик конечной точки использует этот токен для определения параметров прокси-сервера и учетных данных для использования.

</dd> <dt>

*фрефрешонлине* \[ окне\]
</dt> <dd>

Указывает, что погода WUA запрашивает новый маркер. Значение true указывает, что запрашивается новый маркер. Значение false указывает, что запрошен новый или кэшированный токен. Дополнительные сведения см. в разделе "Примечания".

</dd> <dt>

*пбстрендпоинтлок* \[ заполняет\]
</dt> <dd>

Укажите URL-адрес, используемый для взаимодействия со службой. Например, для конечной точки клеинт-Server это будет URL-адрес службы клиентского сервера. Дополнительные сведения см. в разделе "Примечания".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение **\_ ОК** . В противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Комментарии

WUA обычно задает для параметра *фрефрешонлине* значение false при первом вызове этого метода, а затем при возникновении ошибки подключения WUA устанавливает для параметра значение true при повторном вызове метода. Однако реализация этого метода может запросить новый маркер из службы маркеров безопасности (STS) или предоставить кэшированный маркер в любое время.

Если для конечной точки не требуется проверка подлинности, вызывающий объект может подключиться к службе, используя только URL-адрес, указанный параметром *пбстрендпоинтлок* .

Если для конечной точки требуется проверка подлинности, вызывающий объект может использовать URL-адрес, заданный параметром *пбстрендпоинтлок* , и данные, предоставленные другими параметрами.

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

[**иупдатиндпоинтпровидер**](iupdateendpointprovider.md)
</dt> </dl>

 

 




