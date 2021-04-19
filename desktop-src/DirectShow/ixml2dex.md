---
description: Интерфейс IXml2Dex сохраняет и загружает файлы проекта служб редактирования DirectShow (DES) в язык XML (XML). Этот интерфейс также предоставляет методы для чтения и записи файлов графа DirectShow (. ГРФ).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Интерфейс IXml2Dex (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689330"
---
# <a name="ixml2dex-interface"></a>Интерфейс IXml2Dex

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IXml2Dex`Интерфейс сохраняет и загружает файлы проекта [служб редактирования DirectShow](directshow-editing-services.md) (DES) в язык XML (XML). Этот интерфейс также предоставляет методы для чтения и записи файлов графа DirectShow (. ГРФ).

## <a name="members"></a>Элементы

Интерфейс **IXml2Dex** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IXml2Dex** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IXml2Dex** содержит следующие методы.



| Метод                                                      | Описание                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**копиксмл**](ixml2dex-copyxml.md)                         | Не реализован.<br/>                                                |
| [**креатеграффромфиле**](ixml2dex-creategraphfromfile.md) | Не реализован.<br/>                                                |
| [**Удалить**](ixml2dex-delete.md)                           | Не реализован.<br/>                                                |
| [**пастексмл**](ixml2dex-pastexml.md)                       | Не реализован.<br/>                                                |
| [**пастексмлфиле**](ixml2dex-pastexmlfile.md)               | Не реализован.<br/>                                                |
| [**Метода**](ixml2dex-readxml.md)                         | Не реализован.<br/>                                                |
| [**реадксмлфиле**](ixml2dex-readxmlfile.md)                 | Загружает файл XML-проекта.<br/>                                      |
| [**Перезапуск**](ixml2dex-reset.md)                             | Не реализован.<br/>                                                |
| [**вритегрффиле**](ixml2dex-writegrffile.md)               | Записывает граф фильтра в файл в формате ГРФ.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Преобразует временную шкалу в XML-строку.<br/>                         |
| [**вритексмлфиле**](ixml2dex-writexmlfile.md)               | Преобразует временную шкалу в XML и записывает XML-данные в файл.<br/> |
| [**вритексмлпарт**](ixml2dex-writexmlpart.md)               | Не реализован.<br/>                                                |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Internet Explorer 4,0 или более поздней версии<br/>                                               |
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



 

 
