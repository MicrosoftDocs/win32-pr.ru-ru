---
description: интерфейс иамтимелинеобж предоставляет методы для управления объектами временной шкалы в службах DirectShow editing Services (DES).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Интерфейс Иамтимелинеобж (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4a987cfd0f08311a0e7a233ab479e5cdbe2fc649fd521ad4f4ed1b37b6df6d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428164"
---
# <a name="iamtimelineobj-interface"></a>Интерфейс Иамтимелинеобж

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMTimelineObj`интерфейс предоставляет методы для управления объектами временной шкалы в [службах DirectShow editing Services](directshow-editing-services.md) (DES). Все объекты временной шкалы реализуют этот метод, в том числе объекты источника, действия, перехода, трассировки, группы и композиции. Создайте объект временной шкалы, вызвав метод [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) .

## <a name="members"></a>Элементы

Интерфейс **иамтимелинеобж** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамтимелинеобж** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамтимелинеобж** содержит следующие методы.



| Метод                                                          | Описание                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**клеардирти**](iamtimelineobj-cleardirty.md)                 | Не поддерживается.<br/>                                                                                                              |
| [**фикстимес**](iamtimelineobj-fixtimes.md)                     | Округляет указанное время начала и окончания до ближайших границ фрейма.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Округляет указанное время начала и окончания, указанное как значения [**рефтиме**](reftime.md) , на ближайшие границы фрейма.<br/> |
| [**жетдиртиранже**](iamtimelineobj-getdirtyrange.md)           | Не поддерживается.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Не поддерживается.<br/>                                                                                                              |
| [**жетембеддепс**](iamtimelineobj-getembeddepth.md)           | Не поддерживается.<br/>                                                                                                              |
| [**жетженид**](iamtimelineobj-getgenid.md)                     | Извлекает созданный идентификатор объекта.<br/>                                                                                |
| [**жетграупибелонгто**](iamtimelineobj-getgroupibelongto.md)   | Не поддерживается.<br/>                                                                                                              |
| [**Блокировка**](iamtimelineobj-getlocked.md)                   | Возвращает состояние редактирования объекта (заблокировано или разблокировано).<br/>                                                                  |
| [**Выкл.**](iamtimelineobj-getmuted.md)                     | Извлекает состояние отключения объекта.<br/>                                                                                         |
| [**GetPropertyGetter**](iamtimelineobj-getpropertysetter.md)   | Получает метод задания свойства объекта.<br/>                                                                                     |
| [**жетстартстоп**](iamtimelineobj-getstartstop.md)             | Возвращает время начала и окончания объекта относительно родителя объекта.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Извлекает значения времени начала и окончания объекта в виде значений [**рефтиме**](reftime.md) .<br/>                                          |
| [**жетсубобжект**](iamtimelineobj-getsubobject.md)             | Извлекает подобъект, связанный с этим объектом.<br/>                                                                        |
| [**жетсубобжектгуид**](iamtimelineobj-getsubobjectguid.md)     | Извлекает идентификатор GUID для подобъекта, связанного с этим объектом временной шкалы.<br/>                                                   |
| [**жетсубобжектгуидб**](iamtimelineobj-getsubobjectguidb.md)   | Извлекает идентификатор GUID для подобъекта в виде значения **BSTR** .<br/>                                                                    |
| [**жетсубобжектлоадед**](iamtimelineobj-getsubobjectloaded.md) | Определяет, установлен ли указатель на подобъект объекта.<br/>                                                             |
| [**жеттимелиненореф**](iamtimelineobj-gettimelinenoref.md)     | Не поддерживается.<br/>                                                                                                              |
| [**жеттимелинетипе**](iamtimelineobj-gettimelinetype.md)       | Извлекает тип объекта.<br/>                                                                                                |
| [**UserData**](iamtimelineobj-getuserdata.md)               | Извлекает определяемые приложением постоянные данные.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Извлекает определяемый приложением идентификатор объекта.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Извлекает определяемое приложением имя объекта.<br/>                                                                            |
| [**Отменит**](iamtimelineobj-remove.md)                         | Удаляет этот объект с временной шкалы для повторной вставки в другое место.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Окончательно удаляет этот объект из временной шкалы, включая подобъекты и дочерние объекты.<br/>                                       |
| [**сетдиртиранже**](iamtimelineobj-setdirtyrange.md)           | Не реализован.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Не реализован.<br/>                                                                                                            |
| [**сетлоккед**](iamtimelineobj-setlocked.md)                   | Задает для объекта состояние редактирования значение заблокировано или разблокировано.<br/>                                                                      |
| [**сетмутед**](iamtimelineobj-setmuted.md)                     | Задает состояние отключения объекта.<br/>                                                                                              |
| [**сетпропертисеттер**](iamtimelineobj-setpropertysetter.md)   | Задает метод задания свойства объекта.<br/>                                                                                          |
| [**сетстартстоп**](iamtimelineobj-setstartstop.md)             | Задает время начала и окончания объекта относительно временной шкалы.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Задает время начала и окончания работы объекта в виде значений **рефтиме** .<br/>                                                              |
| [**сетсубобжект**](iamtimelineobj-setsubobject.md)             | Не поддерживается.<br/>                                                                                                              |
| [**сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md)     | Указывает глобальный уникальный идентификатор (GUID) подобъекта, связанного с этим объектом.<br/>                               |
| [**сетсубобжектгуидб**](iamtimelineobj-setsubobjectguidb.md)   | Задает идентификатор GUID для подобъекта в виде значения **BSTR** .<br/>                                                                    |
| [**сеттимелинетипе**](iamtimelineobj-settimelinetype.md)       | Не поддерживается.<br/>                                                                                                              |
| [**сетусердата**](iamtimelineobj-setuserdata.md)               | Задает определяемые приложением постоянные данные.<br/>                                                                                   |
| [**сетусерид**](iamtimelineobj-setuserid.md)                   | Задает определяемый приложением идентификатор для объекта.<br/>                                                                      |
| [**сетусернаме**](iamtimelineobj-setusername.md)               | Задает определенное приложением имя для объекта.<br/>                                                                            |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



 

 
