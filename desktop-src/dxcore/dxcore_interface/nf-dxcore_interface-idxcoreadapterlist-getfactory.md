---
title: IDXCoreAdapterList::GetFactory
description: 'Извлекает указатель интерфейса [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) на объект фабрики адаптера дкскоре. | Идкскореадаптерлист:: псевдо'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 97ae5ef0ba321dafaabf1813d943b738f5af4c586050b91712bf9ad93005cb35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094584"
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

## <a name="remarks"></a>Remarks

В течение времени, когда ссылка существует в интерфейсе [идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md) , интерфейсе [идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md) или интерфейсе [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md) , дополнительные вызовы [Дкскорекреатеадаптерфактори](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::]()GetObject или [IDXCoreAdapter::](./nf-dxcore_interface-idxcoreadapter-getfactory.md) GetObject будут возвращать указатели на один и тот же объект, увеличивая число ссылок в интерфейсе **IDXCoreAdapterFactory** .

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)
