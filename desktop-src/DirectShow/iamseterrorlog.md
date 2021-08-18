---
description: интерфейс иамсетеррорлог задает или получает журнал ошибок в службах DirectShow editing Services (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Интерфейс Иамсетеррорлог (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a16e56de7f350b30c1b92c0c94ff3e3e06afc31b363c0b3a6e98017ce483aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756404"
---
# <a name="iamseterrorlog-interface"></a>Интерфейс Иамсетеррорлог

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMSetErrorLog`интерфейс задает или получает журнал ошибок в [службах DirectShow editing Services](directshow-editing-services.md) (DES). Объект временной шкалы реализует этот интерфейс. Приложения могут использовать этот интерфейс для регистрации ошибок отрисовки во время выполнения. Реализуйте интерфейс [**иамеррорлог**](iamerrorlog.md) в приложении, а затем вызовите метод [**иамсетеррорлог::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) на временной шкале.

Дополнительные сведения об использовании этого интерфейса см. в разделе [ведение журнала ошибок](logging-errors.md).

## <a name="members"></a>Элементы

Интерфейс **иамсетеррорлог** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамсетеррорлог** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамсетеррорлог** содержит следующие методы.



| Метод                                               | Описание                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**получить \_ журнал ошибок**](iamseterrorlog-get-errorlog.md) | Извлекает текущий журнал ошибок для данного объекта.<br/> |
| [**Размещение \_ ErrorLog**](iamseterrorlog-put-errorlog.md) | Указывает журнал ошибок для объекта.<br/>           |



 

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



 

 
