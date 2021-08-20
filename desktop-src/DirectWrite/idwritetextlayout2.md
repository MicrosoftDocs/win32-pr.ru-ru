---
title: Интерфейс IDWriteTextLayout2
description: Представляет блок текста после полного анализа и форматирования. | Интерфейс IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Непосредственная запись интерфейса IDWriteTextLayout2
- Непосредственная запись интерфейса IDWriteTextLayout2, описание
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff23fea3d1ae4da7c6dba310ed28dfb8c76d65947426f0219e3868f3859c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816264"
---
# <a name="idwritetextlayout2-interface"></a>Интерфейс IDWriteTextLayout2

Представляет блок текста после полного анализа и форматирования.

## <a name="members"></a>Элементы

Интерфейс **IDWriteTextLayout2** наследует от [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1). **IDWriteTextLayout2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDWriteTextLayout2** содержит следующие методы.



| Метод                                                                                | Описание                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**жетфонтфаллбакк**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Возвращает текущий объект отката шрифта. <br/>                                           |
| [**жетластлиневраппинг**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Возвращает значение, указывающее, упаковано ли Последнее слово в последней строке.<br/>                    |
| [**Метрики**](idwritetextlayout2-getmetrics.md)                                   | Получает общие метрики для форматированной строки. <br/>                             |
| [**жетоптикалалигнмент**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Узнайте, как глифы выровняйте по краям поля. <br/>                               |
| [**жетвертикалглифориентатион**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Получение предпочтительной ориентации глифов при использовании направления чтения по вертикали.<br/> |
| [**сетфонтфаллбакк**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Применение настраиваемого резервного шрифта на макете.<br/>                                        |
| [**сетластлиневраппинг**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Задает, упаковано ли Последнее слово в последней строке. <br/>                   |
| [**сетоптикалалигнмент**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Укажите, как глифы выдаются по краям поля.<br/>                                |
| [**сетвертикалглифориентатион**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Задает предпочтительную ориентацию глифов при использовании направления чтения по вертикали.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

