---
title: DXCoreCreateAdapterFactory
description: Создает фабрику адаптера Дкскоре, которую можно использовать для создания последующих объектов Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 90567d732f6febc5d95b460b2ff88929dd12b2f22275de9db0d6bc5f88ef99ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985184"
---
# <a name="dxcorecreateadapterfactory-function"></a>Функция Дкскорекреатеадаптерфактори

## <a name="description"></a>Описание

Создает фабрику адаптера Дкскоре, которую можно использовать для создания последующих объектов Дкскоре. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="parameters"></a>Параметры

### <a name="riid"></a>riid

Тип: **рефиид**

Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвфактори*. Это должен быть идентификатор интерфейса (IID) [идкскореадаптерфактори](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>Ппвфактори [out]

Тип: **void \* \***

Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* . После успешного возврата *\* ппвфактори* (адрес разыменования) содержит указатель на созданную фабрику дкскоре.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|E_NOINTERFACE|Указано недопустимое значение для *riid*.|
|E_POINTER|`nullptr` был предоставлен для *ппвфактори*.|

## <a name="remarks"></a>Remarks

В течение времени, когда ссылка существует в интерфейсе [идкскореадаптерфактори](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , интерфейсе [идкскореадаптерлист](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) или интерфейсе [идкскореадаптер](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , дополнительные вызовы **Дкскорекреатеадаптерфактори**, [IDXCoreAdapterList::](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)GetObject или [IDXCoreAdapter::](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) GetObject будут возвращать указатели на один и тот же объект, увеличивая число ссылок в интерфейсе **IDXCoreAdapterFactory** .

## <a name="see-also"></a>См. также

[Дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)