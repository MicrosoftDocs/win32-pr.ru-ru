---
title: IDXCoreAdapterList::GetFactory
description: 'Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре. | Идкскореадаптерлист:: псевдо'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105720841"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>Метод Идкскореадаптерлист:: псевдо

Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
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

## <a name="remarks"></a>Комментарии

В течение времени, когда ссылка существует в интерфейсе [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) , интерфейсе [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) или интерфейсе [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) , дополнительные вызовы [Дкскорекреатеадаптерфактори](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::]()GetObject или [IDXCoreAdapter::](./nf-dxcore_interface-idxcoreadapter-getfactory.md) GetObject будут возвращать указатели на один и тот же объект, увеличивая число ссылок в интерфейсе **IDXCoreAdapterFactory** .

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)
