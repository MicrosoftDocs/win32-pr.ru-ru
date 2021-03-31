---
title: Операции Стоклиен
description: В примере Стоклиен показано, как клиент использует структурированное хранилище. Ниже приведена сводка операций Стоклиен.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Операции Стоклиен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792949"
---
# <a name="stoclien-operations"></a>Операции Стоклиен

В примере [стоклиен](structured-storage-client-sample--stoclien-.md) показано, как клиент использует структурированное хранилище. Ниже приведена сводка операций Стоклиен.

Клиентская область окна приложения [стоклиен](structured-storage-client-sample--stoclien-.md) используется для визуального отображения полилиний, созданных с помощью мыши или планшетного устройства. Для рисования с помощью мыши нажмите и удерживайте левую кнопку мыши при перемещении мыши. Отпуская левую кнопку мыши завершает рисование линии.

Ниже приведена сводка операций с точки зрения Stoclien.exe в качестве клиента COM Stoserve.dll сервера COM:

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Файл/открыть
</dt> <dd>

Отображает диалоговое окно Открыть, чтобы получить имя и путь для существующего файла документа, который необходимо открыть. Значение по умолчанию. Предполагается, что для этих файлов используется расширение имени файла PAP. Если при выборе этого пункта меню в существующий рисунок были внесены изменения, то сначала будет отображаться отдельное диалоговое окно с запросом пользователя, если текущий рисунок должен быть сохранен в связанном с ним составном файле.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Файл/сохранить
</dt> <dd>

Сохраняет текущий документ в связанном составном файле.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Файл/сохранить как
</dt> <dd>

Отображает диалоговое окно Сохранить как, чтобы получить имя и путь для нового создаваемого файла документа бумаги. Текущий рисунок преобразуется в сохраненное содержимое нового файла, а новый файл превращается в новый связанный составной файл для рисования.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Файл или выход
</dt> <dd>

Выход из [стоклиен](structured-storage-client-sample--stoclien-.md).

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Рисование и рисование на
</dt> <dd>

Включает рисование между клиентом [стоклиен](structured-storage-client-sample--stoclien-.md) и объектом собумаги на сервере. Эта команда блокирует объект совместной печати для монопольного использования этим клиентом и предотвращает доступ других клиентов к тому же экземпляру совместной бумаги на сервере.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Рисование и рисование
</dt> <dd>

Отключает Рисование между клиентом [стоклиен](structured-storage-client-sample--stoclien-.md) и объектом собумаги на сервере. Эта команда разблокирует собумагу для монопольного использования этим клиентом и позволяет другим клиентам получить доступ к тому же экземпляру совместной бумаги на сервере.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Рисование и перерисовка
</dt> <dd>

Перерисовывает в клиенте текущие данные рисования, удерживаемые в объекте собумаги на сервере.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Рисование и стирание
</dt> <dd>

Удаляет текущее содержимое рисунка и очищает изображение окна. Выбор в меню: перо/цвет отображает диалоговое окно Выбор цвета для получения нового цвета пера для рисования.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Перо/средний
</dt> <dd>

Выбирает среднюю ширину для рисования. Галочка в этом варианте меню означает, что средняя — это текущая ширина пера.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Перо/толстое
</dt> <dd>

Выбирает жирную ширину для рисования. Галочка в этом варианте меню означает, что жирная ширина является текущей толщиной пера.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Перо или тонкий
</dt> <dd>

Выбирает тонкую ширину для рисования. Галочка в этом меню указывает на то, что тонкий цвет является текущей толщиной пера.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Приемник/подключение
</dt> <dd>

Подключает интерфейс Копаперсинк Ипаперсинк к точке подключения объекта кобумага Паперсинк. Перерисовка текущего изображения рисунка в [стоклиен](structured-storage-client-sample--stoclien-.md) полагается на соединение приемника. Галочка в этом варианте меню означает, что перерисовка подключена.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Приемник/отключение
</dt> <dd>

Отключает интерфейс Копаперсинк Ипаперсинк от объекта кодокументной Паперсинк точки подключения. Перерисовка текущего изображения рисунка в [стоклиен](structured-storage-client-sample--stoclien-.md) полагается на соединение приемника. Галочка в этом варианте меню означает, что перерисовка отключена.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Руководство по справке и Стоклиен
</dt> <dd>

Открывает STOCLIEN.HTM файл учебника в веб-браузере.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Руководство по справке и Стосерве
</dt> <dd>

Открывает STOSERVE.HTM файл учебника в веб-браузере.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Файл исходного кода справки или чтения
</dt> <dd>

Открывает диалоговое окно Открыть, в котором можно открыть исходный файл из этого занятия или другого файла в блокноте Windows.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Справка/о Стоклиен
</dt> <dd>

Отображает диалоговое окно "о программе" для этого приложения.

</dd> </dl>

В примере [стоклиен](structured-storage-client-sample--stoclien-.md) используются многие служебные классы и службы, предоставляемые [аппутил](./using-visual-studio.md). Дополнительные сведения о [аппутил](./using-visual-studio.md)см. в разделе исходный код библиотеки [аппутил](./using-visual-studio.md) в каталоге одноуровневых [аппутил](./using-visual-studio.md) и Apputil.md в главном каталоге Tutorial. Дополнительные сведения о [аппутил](./using-visual-studio.md)см. [в разделе Создание образцов](how-to-build-samples.md).

 

 