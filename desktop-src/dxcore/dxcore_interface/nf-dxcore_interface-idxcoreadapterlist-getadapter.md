---
title: IDXCoreAdapterList::GetAdapter
description: Извлекает конкретный адаптер по индексу из объекта списка адаптеров Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070431"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>Метод Идкскореадаптерлист:: Adapter

Извлекает конкретный адаптер по индексу из объекта списка адаптеров Дкскоре. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Параметры

### <a name="index"></a>index

Тип: **uint32_t**

Отсчитываемый от нуля индекс, идентифицирующий экземпляр адаптера в списке адаптеров Дкскоре.

### <a name="riid"></a>riid

Тип: **рефиид**

Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в *ппвадаптер*. Это должен быть идентификатор интерфейса (IID) [идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md).

### <a name="ppvadapter-out"></a>Ппвадаптер [out]

Тип: **void \* \***

Адрес указателя на интерфейс с идентификатором IID, указанным в параметре *riid* . После успешного возврата *\* ппвадаптер* (адрес разыменования) содержит указатель на созданный адаптер дкскоре.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|*Индекс* действителен, но адаптер больше не находится в допустимом состоянии.|
|E_INVALIDARG|Указан недопустимый *индекс* .|
|E_NOINTERFACE|Указано недопустимое значение для *riid*.|
|E_POINTER|`nullptr` был предоставлен для *ппвадаптер*.|

## <a name="remarks"></a>Комментарии

Несколько вызовов, передающих индекс, представляющий тот же адаптер, возвращают идентичные указатели интерфейса, даже в разных списках адаптеров. В результате можно сравнивать указатели интерфейса, чтобы определить, ссылаются ли несколько указателей на один и тот же объект адаптера.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерлист](./nn-dxcore_interface-idxcoreadapterlist.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)