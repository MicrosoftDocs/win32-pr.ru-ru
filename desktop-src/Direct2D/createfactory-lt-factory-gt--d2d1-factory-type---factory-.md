---
title: Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
description: Создает объект фабрики, который можно использовать для создания ресурсов Direct2D. | Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Фабрика D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory), функция Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af5635a6f996ea6cd3af2c3b3022efa054cd27605430c8230143980e00b9abbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826473"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><Factory>Функция D2D1CreateFactory ( \_ Тип фабрики D2D1 \_ , фабрика \* \* )

Создает объект фабрики, который можно использовать для создания ресурсов Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Параметры шаблона



| Параметр | Описание                                                 |
|-----------|-------------------------------------------------------------|
| *Установлен* | Тип создаваемого [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . |



 

## <a name="parameters"></a>Параметры



| Параметр     | Описание                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | Потоковая модель фабрики и создаваемые ею ресурсы.                |
| *фабрика*     | При возврате из этого метода содержит адрес указателя на новую фабрику. |



 

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="examples"></a>Примеры

В следующем примере создается фабрика.


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для приложений для \[ классических приложений Windows Vista \|\]<br/>                          |
| Минимальная версия сервера<br/> | Windows сервер 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008 приложения \[ UWP для классических приложений \|\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Библиотека<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

