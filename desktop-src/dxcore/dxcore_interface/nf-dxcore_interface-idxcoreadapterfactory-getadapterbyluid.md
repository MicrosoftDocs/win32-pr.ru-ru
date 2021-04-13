---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Возвращает объект адаптера Дкскоре ([идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md)) для указанного LUID, если он доступен.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413387"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>Метод Идкскореадаптерфактори:: Жетадаптербилуид

Возвращает объект адаптера Дкскоре ([идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md)) для указанного LUID, если он доступен. Инструкции по программированию и примеры кода см. [в разделе Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Параметры

### <a name="adapterluid"></a>адаптерлуид

Тип: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

Локально уникальное значение, идентифицирующее экземпляр адаптера.

### <a name="riid-in"></a>riid [in]

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
|DXGI_ERROR_DEVICE_REMOVED|LUID адаптера, переданный в *адаптерлуид* , распознан, но адаптер больше не находится в допустимом состоянии.|
|E_INVALIDARG|Такой LUID адаптера отсутствует, так как значение, переданное в *адаптерлуид* , доступно через дкскоре.|
|E_NOINTERFACE|Указано недопустимое значение для *riid*.|
|E_POINTER|`nullptr` был предоставлен для *ппвадаптер*.|

## <a name="remarks"></a>Комментарии

Несколько вызовов, передающих один и тот же [LUID](/windows/win32/api/winnt/ns-winnt-luid) , возвращают идентичные указатели интерфейса. В результате можно сравнивать указатели интерфейса, чтобы определить, ссылаются ли несколько указателей на один и тот же объект адаптера.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптерфактори](./nn-dxcore_interface-idxcoreadapterfactory.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)