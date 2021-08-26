---
description: интерфейс иамтимелиниффектабле предоставляет методы для добавления эффектов к объекту временной шкалы в службах DirectShow editing Services (DES), а также для управления эффектами на объекте.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Интерфейс Иамтимелиниффектабле (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ad6b373f4b30209566709117b3b15ecf1a65d093ddb2dd27e9e0273b11ad0b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905034"
---
# <a name="iamtimelineeffectable-interface"></a>Интерфейс Иамтимелиниффектабле

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMTimelineEffectable`интерфейс предоставляет методы для добавления эффектов к объекту временной шкалы в [службах DirectShow editing Services](directshow-editing-services.md) (DES) и для управления эффектами на объекте. Этот интерфейс реализуется всеми объектами, к которым могут применяться эффекты. Сюда входят источники, дорожки и композиции.

Объект, реализующий этот интерфейс, может иметь любое количество эффектов. Для каждого объекта механизм визуализации применяет свои эффекты в порядке приоритета, начиная с уровня приоритета 0.

## <a name="members"></a>Элементы

Интерфейс **иамтимелиниффектабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамтимелиниффектабле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамтимелиниффектабле** содержит следующие методы.



| Метод                                                                     | Описание                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**еффектжеткаунт**](iamtimelineeffectable-effectgetcount.md)             | Возвращает количество эффектов для данного объекта.<br/>                    |
| [**еффектинсбефоре**](iamtimelineeffectable-effectinsbefore.md)           | Вставляет результат в объект с указанным уровнем приоритета.<br/> |
| [**еффектсвапприоритиес**](iamtimelineeffectable-effectswappriorities.md) | Переключает уровни приоритета двух эффектов.<br/>                       |
| [**Действие**](iamtimelineeffectable-geteffect.md)                       | Получает результат на указанном уровне приоритета.<br/>              |



 

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



 

 
