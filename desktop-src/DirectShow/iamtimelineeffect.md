---
description: интерфейс иамтимелиниффект предоставляет методы для управления звуковыми и видеоэффектами в службах DirectShow editing Services (DES).
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
ms.openlocfilehash: f710693c967e1f0ac73c69534e8ac90a65d6603e749cd2aeae6a355ed8517415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052764"
---
# <a name="iamtimelineeffect-interface"></a>Интерфейс Иамтимелиниффект

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMTimelineEffect`интерфейс предоставляет методы для управления звуковыми и видеоэффектами в [службах DirectShow editing Services](directshow-editing-services.md) (DES). К любому объекту временной шкалы, предоставляющему интерфейс [**иамтимелиниффектабле**](iamtimelineeffectable.md) , можно добавить эффекты. Чтобы задать свойства для влияния, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .

Объект влияния DES на самом деле является оболочкой для одного из двух других объектов:

-   для звуковых эффектов любой DirectShow фильтр звукового эффекта.
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



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Работа с эффектами и переходами](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
