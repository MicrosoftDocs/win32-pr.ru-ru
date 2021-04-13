---
title: Примеры анимации Windows
description: Разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по диспетчеру анимации Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Анимация Windows, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331643"
---
# <a name="windows-animation-samples"></a>Примеры анимации Windows

Разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по диспетчеру анимации Windows.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                     | Описание                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Пример анимации на основе приложений](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Пример анимации на основе таймера](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Пользовательский пример интерполяции](custom-interpolator-sample.md)<br/>                   | Показывает, как использовать анимацию Windows с собственным пользовательским интерполяцией с Direct2D, используемой для отрисовки. <br/> |
| [Образец макета сетки](grid-layout-sample.md)<br/>                                   | Показывает, как использовать анимацию Windows с помощью Direct2D для анимации сетки изображений. <br/>                         |
| [Пример сравнения приоритетов](priority-comparison-sample.md)<br/>                   | Показывает, как использовать анимацию Windows с собственным сравнением приоритетов с помощью Direct2D для подготовки к просмотру.<br/>      |



 

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Руководством по разработке анимации Windows](windows-animation-developer-guide.md)
</dt> <dt>

[Справочник по анимации Windows](windows-animation-reference.md)
</dt> </dl>

 

 





