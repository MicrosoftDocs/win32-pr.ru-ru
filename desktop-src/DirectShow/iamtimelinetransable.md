---
description: интерфейс иамтимелинетрансабле добавляет переходы к объекту в службах DirectShow editing Services (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Интерфейс Иамтимелинетрансабле (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6228b836f85251dda7f43d6c3b421d486b727c6bdc6c319b9cf7ca1e37d34a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052034"
---
# <a name="iamtimelinetransable-interface"></a>Интерфейс Иамтимелинетрансабле

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMTimelineTransable`интерфейс добавляет переходы к объекту в [DirectShow служб редактирования](directshow-editing-services.md) (DES). Этот интерфейс предоставляется любым объектом, к которому могут применяться переходы, включая записи, композиции и группы. Объект, реализующий этот интерфейс, может иметь любое количество переходов, но переходы не должны перекрываться по времени.

> [!Note]  
> Звук не поддерживает переходы. Объекты внутри звуковых групп могут предоставлять `IAMTimelineTransable` интерфейс, но приложение не должно добавлять к ним переходы.

 

## <a name="members"></a>Элементы

Интерфейс **иамтимелинетрансабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамтимелинетрансабле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамтимелинетрансабле** содержит следующие методы.



| Метод                                                          | Описание                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**жетнексттранс**](iamtimelinetransable-getnexttrans.md)       | Извлекает первый переход, который отображается в указанное время или позже.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Извлекает первый переход, который отображается в указанное время или более поздней версии, с временем, указанным в качестве значения **рефтиме** .<br/> |
| [**жеттрансаттиме**](iamtimelinetransable-gettransattime.md)   | Извлекает переход, ближайший к указанному времени.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Получает ближайшее к указанному времени переход, заданный как значение **рефтиме** .<br/>                                   |
| [**трансадд**](iamtimelinetransable-transadd.md)               | Добавляет переход к объекту.<br/>                                                                                        |
| [**трансжеткаунт**](iamtimelinetransable-transgetcount.md)     | Возвращает число переходов для данного объекта.<br/>                                                                     |



 

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



 

 
