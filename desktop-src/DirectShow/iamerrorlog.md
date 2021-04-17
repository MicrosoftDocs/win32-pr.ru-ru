---
description: Интерфейс Иамеррорлог предоставляет метод обратного вызова для ведения журнала ошибок в службах редактирования DirectShow (DES). DES не реализует этот интерфейс.
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
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675302"
---
# <a name="iamerrorlog-interface"></a>Интерфейс Иамеррорлог

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMErrorLog`Интерфейс предоставляет метод обратного вызова для ведения журнала ошибок в [службах редактирования DirectShow](directshow-editing-services.md) (DES).

DES не реализует этот интерфейс. Чтобы выполнить ведение журнала ошибок, реализуйте этот интерфейс в приложении и вызовите [**иамсетеррорлог::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) на временной шкале. Если при подготовке проекта к просмотру возникает ошибка, то DES вызывает метод [**иамеррорлог:: LogError**](iamerrorlog-logerror.md) , реализованный приложением.

DES регистрирует ошибки только при отрисовке проекта с помощью интерфейса [**ирендеренгине**](irenderengine.md) . Например, если вы сохраняете проект в виде графа фильтра DirectShow (формат ГРФ) и воспроизводите файл графа, ведение журнала ошибок отсутствует. Дополнительные сведения об использовании этого интерфейса см. в разделе [ведение журнала ошибок](logging-errors.md).

## <a name="members"></a>Элементы

Интерфейс **иамеррорлог** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамеррорлог** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамеррорлог** содержит следующие методы.



| Метод                                   | Описание               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Заносит в журнал ошибку.<br/> |



 

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



 

 
