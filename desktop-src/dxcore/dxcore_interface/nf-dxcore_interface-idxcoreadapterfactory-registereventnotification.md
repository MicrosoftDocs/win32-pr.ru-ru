---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Регистрируется для получения уведомлений о конкретных условиях из адаптера Дкскоре или из списка адаптеров.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b97b51f7c4359526317647b62241e37063243a56f45014c28ba2f2cd897706ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042902"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>Метод Идкскореадаптерфактори:: Регистеревентнотификатион

Регистрируется для получения уведомлений о конкретных условиях из адаптера Дкскоре или из списка адаптеров. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="dxcoreobject-in"></a>Дкскореобжект [in]

Тип: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Объект Дкскоре ([идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) или [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md)), чьи уведомления подписаны на.

### <a name="notificationtype"></a>notificationType

Тип: **[дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md)**

Тип уведомления, для которого выполняется регистрация. Сведения о типах, допустимых для типов объектов, см. в таблице в [дкскоренотификатионтипе](./ne-dxcore_interface-dxcorenotificationtype.md) .

### <a name="callbackfunction-in"></a>Каллбаккфунктион [in]

Тип: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Указатель на функцию обратного вызова (реализованную приложением), который вызывается объектом Дкскоре для событий уведомления. Сигнатура функции см. в разделе [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackContext [in]

Тип: **void \***

Необязательный указатель на объект, содержащий сведения о контексте. Этот объект передается функции обратного вызова при возникновении уведомления.

### <a name="eventcookie-out"></a>Евенткукие [out]

Тип: **uint32_t \***

Указатель на значение **uint32_t** . В случае успеха функция отменяет ссылку на указатель и присваивает значение ненулевому значению cookie, представляющему эту регистрацию. Используйте это значение файла cookie для отмены регистрации в уведомлении путем вызова [идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). См. **Примечания**.

В случае неудачи функция отменяет ссылку на указатель и устанавливает значение равным нулю, которое представляет недопустимое значение cookie.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DXGI_ERROR_INVALID_CALL|*нотификатионтипе* не поддерживается операционной системой (ОС).|
|E_INVALIDARG|`nullptr` был предоставлен для *дкскореобжект* или если было предоставлено недопустимое сочетание *нотификатионтипе* и *дкскореобжект* .|
|E_POINTER|`nullptr` был предоставлен для *каллбаккфунктион* или *евенткукие*.|

## <a name="remarks"></a>Remarks

**Регистеревентнотификатион** используется для регистрации событий, вызванных интерфейсами [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) и [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) . Эти типы уведомлений поддерживаются.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|Поддерживаемые *дкскореобжект*|Примечания|
|-|-|-|
|адаптерлистстале|**IDXCoreAdapterList**|Указывает, что список адаптеров, отвечающих условиям фильтра, изменился. Если список адаптеров устарел во время регистрации, метод обратного вызова вызывается немедленно. Этот обратный вызов выполняется не чаще одного раза на регистрацию.|
|адаптернолонжервалид|**IDXCoreAdapter**|Указывает, что адаптер больше не действителен. Если во время регистрации адаптер является недопустимым, то метод обратного вызова вызывается немедленно.|
|адаптербуджетчанже|**IDXCoreAdapter**|Указывает, что произошло событие бюджетирования памяти, и необходимо вызвать [идкскореадаптер:: куеристате](./nf-dxcore_interface-idxcoreadapter-querystate.md) (WITH [Дкскореадаптерстате:: адаптермеморибуджет](./ne-dxcore_interface-dxcoreadapterstate.md)) для вычисления текущего состояния бюджета памяти. После регистрации всегда будет выполняться начальный обратный вызов, позволяющий запрашивать начальное состояние.|
|адаптерхардвареконтентпротектионтеардовн|**IDXCoreAdapter**|Указывает, что необходимо повторно оценить текущее состояние сеанса шифрования; Например, путем вызова [ID3D11VideoContext1:: чекккриптосессионстатус](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) , чтобы определить влияние аппаратного уничтожения на определенный интерфейс [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) . После регистрации всегда будет выполняться начальный обратный вызов, позволяющий запрашивать начальное состояние.|

Вызов функции, предоставляемой в *каллбаккфунктион* , выполняется асинхронно в фоновом потоке дкскоре при возникновении обнаруженного события. Нет никакой гарантии на порядок или время обратных вызовов &mdash; . несколько обратных вызовов могут выполняться в любом порядке или даже одновременно. Можно даже вызвать обратный вызов до завершения **регистеревентнотификатион** . В этом случае Дкскоре гарантирует, что *евенткукие* задается перед вызовом обратного вызова. Несколько обратных вызовов для определенной регистрации будут сериализованы по порядку.

Обратные вызовы могут происходить в любое время до вызова [унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)и завершения. Обратные вызовы происходят в собственных потоках, и вы можете вызывать API Дкскоре в этих потоках, в том числе **унрегистеревентнотификатион**. Однако не следует освобождать последнюю ссылку на *дкскореобжект* в этом потоке.

> [!IMPORTANT]
> Перед уничтожением объекта Дкскоре, представленного аргументом *дкскореобжект* , переданным в **регистеревентнотификатион**, необходимо использовать значение cookie для отмены регистрации этого объекта из уведомлений путем вызова [идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Если этого не сделать, то при обнаружении ситуации будет создано неустранимое исключение.

## <a name="see-also"></a>См. также

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Использование DXCore для перечисления адаптеров](../dxcore-enum-adapters.md)