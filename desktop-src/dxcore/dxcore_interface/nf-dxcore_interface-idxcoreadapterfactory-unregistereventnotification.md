---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Отменяет регистрацию в уведомлении, которое вы ранее зарегистрировали для.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 64fb54226f1fad0d1d36f8f4260c9c9172b105dc6239ea5cb805c32b57a938ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278885"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>Метод Идкскореадаптерфактори:: Унрегистеревентнотификатион

Отменяет регистрацию в уведомлении, которое вы ранее зарегистрировали для. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="eventcookie"></a>евенткукие

Тип: **uint32_t**

Значение файла cookie (возвращается при вызове [идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)), представляющем ранее зарегистрированную регистрацию, для которой теперь нужно отменить регистрацию.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|E_INVALIDARG|Значение *евенткукие* не является допустимым файлом cookie, представляющим прошлую регистрацию.|

## <a name="remarks"></a>Remarks

**Унрегистеревентнотификатион** возвращает только после завершения всех обратных вызовов и ожидающих выполнения для этой регистрации. Дкскоре гарантирует, что для этой регистрации не будут выполняться новые обратные вызовы после возвращения **унрегистеревентнотификатион** . Однако во избежание взаимоблокировки при вызове **унрегистеревентнотификатион** из функции обратного вызова **унрегистеревентнотификатион** не ждет завершения активного обратного вызова.

> [!IMPORTANT]
> Перед уничтожением объекта Дкскоре, представленного аргументом *дкскореобжект* , переданным в [Идкскореадаптерфактори:: регистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), необходимо использовать значение cookie для отмены регистрации этого объекта из уведомлений путем вызова **унрегистеревентнотификатион**. Если этого не сделать, то при обнаружении ситуации будет создано неустранимое исключение.

После отмены регистрации значения cookie это значение может быть возвращено последующей регистрацией.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [идкскореадаптерфактори:: унрегистеревентнотификатион](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Использование DXCore для перечисления адаптеров](../dxcore-enum-adapters.md)