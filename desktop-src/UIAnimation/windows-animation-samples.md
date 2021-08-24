---
title: Windows Примеры анимации
description: разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по Windowsию анимации.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Windows анимация Windows анимации, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9119ab7333f1f5d74b9be9998ad26b36139f9a92d88fec856d3f4572d12f431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656154"
---
# <a name="windows-animation-samples"></a>Windows Примеры анимации

разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по Windowsию анимации.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                     | Описание                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Пример анимации на основе приложений](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Пример анимации на основе таймера](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Пользовательский пример интерполяции](custom-interpolator-sample.md)<br/>                   | показывает, как использовать анимацию Windows с собственным пользовательским интерполяцией с Direct2D, используемой для отрисовки. <br/> |
| [Образец макета сетки](grid-layout-sample.md)<br/>                                   | демонстрирует использование Windows анимации с помощью Direct2D для анимации сетки изображений. <br/>                         |
| [Пример сравнения приоритетов](priority-comparison-sample.md)<br/>                   | показывает, как использовать анимацию Windows с собственным сравнением приоритетов с помощью Direct2D для подготовки к просмотру.<br/>      |



 

## <a name="sample-files"></a>Файлы образца

Каждый пример содержит множество следующих файлов ключей:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp
</dt> <dd>

Определяет точку входа приложения.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h
</dt> <dd>

Объявляет класс Кмаинвиндов.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp
</dt> <dd>

Инициализирует компоненты анимации и графическую платформу, загружает изображения и готовит к просмотру клиентской области.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>Лайаутманажер. h
</dt> <dd>

Объявляет класс Клайаутманажер.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>Лайаутманажер. cpp
</dt> <dd>

Вычисляет макет изображений в главном окне, создает раскадровки, добавляет переходы в раскадровку и планирует раскадровку.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail. h
</dt> <dd>

Объявляет класс Ксумбнаил.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Эскиз. cpp
</dt> <dd>

Создает переменные анимации и визуализирует эскизы.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Рекомендации по разработке анимации](windows-animation-developer-guide.md)
</dt> <dt>

[Windows Справочник по анимации](windows-animation-reference.md)
</dt> </dl>

 

 





