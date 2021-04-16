---
description: Интерфейс Иамтимелиниффект предоставляет методы для управления звуковыми и видеоэффектами в службах редактирования DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Интерфейс Иамтимелиниффект (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680072"
---
# <a name="iamtimelineeffect-interface"></a>Интерфейс Иамтимелиниффект

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMTimelineEffect`Интерфейс предоставляет методы для управления звуковыми и видеоэффектами в [службах редактирования DirectShow](directshow-editing-services.md) (DES). К любому объекту временной шкалы, предоставляющему интерфейс [**иамтимелиниффектабле**](iamtimelineeffectable.md) , можно добавить эффекты. Чтобы задать свойства для влияния, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .

Объект влияния DES на самом деле является оболочкой для одного из двух других объектов:

-   Для звуковых эффектов — любой фильтр звукового эффекта DirectShow.
-   Для видеоэффектов и 1-входного объекта преобразования DirectX.

Корпорация Майкрософт больше не поддерживает разработку объектов преобразования DirectX сторонних производителей.

Чтобы указать фильтр или объект преобразования DirectX для воздействия, вызовите метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) .

Чтобы создать объект Effect, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) с помощью \_ действия основной тип временной шкалы \_ \_ . Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для `IAMTimelineEffect` интерфейса.

## <a name="members"></a>Элементы

Интерфейс **иамтимелиниффект** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамтимелиниффект** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамтимелиниффект** содержит следующие методы.



| Метод                                                           | Описание                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**еффектжетприорити**](iamtimelineeffect-effectgetpriority.md) | Получает уровень приоритета воздействия.<br/> |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Работа с эффектами и переходами](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
