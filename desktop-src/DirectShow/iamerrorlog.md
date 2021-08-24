---
description: интерфейс иамеррорлог предоставляет метод обратного вызова для регистрации ошибок в службах DirectShow editing Services (DES). DES не реализует этот интерфейс.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Интерфейс Иамеррорлог (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f2edd1d315cc7ae35bbc200209667d49d53392ce86a10b40a067182cd0621124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756464"
---
# <a name="iamerrorlog-interface"></a>Интерфейс Иамеррорлог

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMErrorLog`интерфейс предоставляет метод обратного вызова для регистрации ошибок в [службах DirectShow editing Services](directshow-editing-services.md) (DES).

DES не реализует этот интерфейс. Чтобы выполнить ведение журнала ошибок, реализуйте этот интерфейс в приложении и вызовите [**иамсетеррорлог::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) на временной шкале. Если при подготовке проекта к просмотру возникает ошибка, то DES вызывает метод [**иамеррорлог:: LogError**](iamerrorlog-logerror.md) , реализованный приложением.

DES регистрирует ошибки только при отрисовке проекта с помощью интерфейса [**ирендеренгине**](irenderengine.md) . например, если вы сохраняете проект в виде графа фильтра DirectShow (формат грф) и воспроизводите файл графа, ведение журнала ошибок отсутствует. Дополнительные сведения об использовании этого интерфейса см. в разделе [ведение журнала ошибок](logging-errors.md).

## <a name="members"></a>Элементы

Интерфейс **иамеррорлог** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамеррорлог** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамеррорлог** содержит следующие методы.



| Метод                                   | Описание               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Заносит в журнал ошибку.<br/> |



 

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



 

 
