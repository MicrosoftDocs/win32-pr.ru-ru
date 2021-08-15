---
title: IDXCoreAdapter::GetFactory
description: 'Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре. | Идкскореадаптер:: псевдо'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 759960875f67acefabf9f4207a9ea38150757b0b2bbec673e6feed3b0c197ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279467"
---
# <a name="idxcoreadaptergetfactory-method"></a>Метод Идкскореадаптер:: псевдо

Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Параметры

### <a name="riid"></a>riid

Тип: **рефиид**

Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвфактори*. Это должен быть идентификатор интерфейса (IID) [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>Ппвфактори [out]

Тип: **void \* \***

Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* . После успешного возврата *\* ппвфактори* (адрес разыменования) содержит указатель на существующий объект фабрики адаптера дкскоре. Перед возвращением функция увеличивает счетчик ссылок в интерфейсе [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) объекта фабрики.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|E_NOINTERFACE|Указано недопустимое значение для *riid*.|
|E_POINTER|`nullptr` был предоставлен для *ппвфактори*.|

## <a name="remarks"></a>Remarks

В течение времени, когда ссылка существует в интерфейсе [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) , интерфейсе [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) или интерфейсе [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) , дополнительные вызовы [Дкскорекреатеадаптерфактори](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)GetObject или [IDXCoreAdapter::]() GetObject будут возвращать указатели на один и тот же объект, увеличивая число ссылок в интерфейсе **IDXCoreAdapterFactory** .

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)
