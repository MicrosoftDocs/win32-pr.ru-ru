---
title: Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Создает объект фабрики, который можно использовать для создания ресурсов Direct2D. | Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Фабрика D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory), функция Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34cbe566b139ebd873e8e9895aa21307113be9632b2045d40c099f52f49fc574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824694"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>D2D1CreateFactory <Factory> ( \_ Тип фабрики D2D1 \_ , \_ параметры фабрики D2D1 \_&, Factory \* \* )

Создает объект фабрики, который можно использовать для создания ресурсов Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Параметры шаблона



| Параметр | Описание                                                 |
|-----------|-------------------------------------------------------------|
| *Установлен* | Тип создаваемого [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . |



 

## <a name="parameters"></a>Параметры



| Параметр        | Описание                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | Потоковая модель фабрики и создаваемые ею ресурсы.                |
| *факторйоптионс* | Уровень детализации, предоставляемый слою отладки.                            |
| *фабрика*        | При возврате из этого метода содержит адрес указателя на новую фабрику. |



 

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для приложений для \[ классических приложений Windows Vista \|\]<br/>                          |
| Минимальная версия сервера<br/> | Windows сервер 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008 приложения \[ UWP для классических приложений \|\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Заголовок<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Библиотека<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

