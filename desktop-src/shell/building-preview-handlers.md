---
description: В этом разделе обсуждаются конкретные интерфейсы и методы, необходимые для создания обработчика просмотра.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Создание обработчиков предварительного просмотра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342852"
---
# <a name="building-preview-handlers"></a>Создание обработчиков предварительного просмотра

В этом разделе обсуждаются конкретные интерфейсы и методы, необходимые для создания обработчика просмотра.

Обработчик просмотра должен реализовывать следующие интерфейсы:

-   [IInitializeWithStream:: Initialize](#iinitializewithstreaminitialize) (настоятельно рекомендуется), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)или [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [иолевиндов](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Если обработчик просмотра поддерживает визуальные параметры, предоставляемые узлом, например цвет фона и шрифт, он должен также реализовать следующий интерфейс:

-   [ипревиевхандлервисуалс](#ipreviewhandlervisuals)

В этом разделе предполагается, что обработчик просмотра инициализируется потоком и зарегистрирован для определенного расширения имени файла.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream:: Initialize

Сохраните параметры [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) и Mode, чтобы вы могли считывать данные элемента, когда будете готовы к предварительному просмотру элемента. Не загружайте данные в [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Загрузите данные в [**IPreviewHandler::D опревиев**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) непосредственно перед отрисовкой.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite:: SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite::-сайт](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite:: SetSite

Сохраните указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для последующего доступа.

Если в настоящее время имеется ссылка на объект [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) , освободите его. Используйте сохраненный указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для вызова [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на сайте для новой ссылки **IPreviewHandlerFrame** .

Если у вас уже есть таблица сочетаний клавиш, удалите ее. Вызовите [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) , чтобы получить новую таблицу сочетаний клавиш. Сохранить эту таблицу. Обратите внимание, что он используется только в качестве списка сочетаний клавиш, поддерживаемых кадром. Команды в записи ускорителя игнорируются.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite::-сайт

Возврат указателя сайта, независимо от его значения.

## <a name="iolewindow"></a>иолевиндов

-   [Иолевиндов:: Контекстсенситивехелп](#iolewindowcontextsensitivehelp)
-   [Иолевиндов::/Window](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>Иолевиндов:: Контекстсенситивехелп

\_Для этого метода возвращается E нотимпл.

### <a name="iolewindowgetwindow"></a>Иолевиндов::/Window

Если окно обработчика просмотра в данный момент существует, возвратите **HWND** этого окна и \_ ОК. Если окно не существует, возвращается значение E \_ Fail.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler:: Сетвиндов](#ipreviewhandlersetwindow)
-   [IPreviewHandler:: SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D Опревиев](#ipreviewhandlerdopreview)
-   [IPreviewHandler:: SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler:: Куерифокус](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler:: TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler:: unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler:: Сетвиндов

Установите параметр *HWND* этого метода в родительский элемент **HWND** обработчика просмотра. Этот метод можно вызывать несколько раз. Измените размер предварительной версии так, чтобы она отображалась только в области, описанной параметром *PRC* .

Если предварительный просмотр находится в процессе подготовки к просмотру, используйте метод [**IPreviewHandler:: сетвиндов**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) , чтобы изменить родительский элемент для предварительного просмотра. Также измените область, в которой будет отображаться предварительный просмотр.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler:: SetRect

Измените размер предварительной версии так, чтобы она отображалась только в области, описанной в этом методе ( *PRC*).

Если средство просмотра находится в процессе подготовки к просмотру, измените область, в которой будет отображаться средство предварительного просмотра.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D Опревиев

Именно здесь выполняется реальная работа. Так как предварительная версия является динамической, содержимое для предварительного просмотра должно загружаться только тогда, когда оно требуется. Не загружайте содержимое в инициализацию.

Если окно обработчика просмотра не существует, создайте его. Окна обработчика просмотра должны быть дочерними по отношению к окну, предоставленному [**IPreviewHandler:: сетвиндов**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Они должны иметь размер, предоставляемый **IPreviewHandler:: сетвиндов** и [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (в зависимости от того, что вызывалось наиболее часто).

После создания окна Загрузите данные из [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , который был инициализирован обработчиком просмотра, и выводит эти данные в окно обработчика просмотра.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler:: SetFocus

Этот метод вызывается, когда фокус переходит на панель чтения с помощью действия Tab. Так как его можно указать в качестве вкладки пересылки или обратную табуляцию, используйте текущее состояние клавиши SHIFT, чтобы решить, должна ли фокус первой или последней позиции табуляции на панели чтения.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler:: Куерифокус

Этот метод должен вызывать функцию [**Focus**](/windows/win32/api/winuser/nf-winuser-getfocus) и возвращать результат этого вызова в параметре *ФВНД* .

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler:: TranslateAccelerator

Этот метод вызывается конвейером сообщений процесса обработчика просмотра (prevhost.exe или настраиваемого локального сервера) в ответ на нажатие клавиш пользователя. Обработчики просмотра должны обменять эти нажатия клавиш или пересылать их на свои узлы в соответствии с алгоритмом, описанным ниже.

Тем не менее, поскольку предварительные версии доступны только для чтения, ввод с клавиатуры должен быть минимальным и оптимизацией, например, в большинстве случаев не требуется.

Если сочетание клавиш, переданное этому методу с помощью конвейера сообщений, является ускорителем, который принимает обработчик предварительного просмотра, обработайте его и возвратит S \_ ОК. Если обработчик не принимает этот ускоритель, сообщение ускорителя может быть отправлено назад, как и обрабатываемый кадр.

Есть два варианта перенаправления сочетаний клавиш в рамку:

Простейшая модель заключается в пересылке всех нажатий клавиш на узел с помощью [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Это делается в образце обработчика просмотра, который предоставляется в пакете SDK для Windows. Все обработчики предварительной версии с низким уровнем целостности должны использовать эту модель. Если ускоритель не обрабатывается обработчиком просмотра, вызовите метод **IPreviewHandlerFrame:: TranslateAccelerator** и возвратите его результат.

Другая модель заключается в использовании таблицы сочетаний клавиш в качестве оптимизации, чтобы избежать отправки слишком большого количества нажатий клавиш через границы процесса:

1.  Когда в обработчике просмотра вызывается [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) , получите таблицу сочетаний клавиш через [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). (Не забудьте освободить маркер в таблице сочетаний клавиш при уничтожении предварительного просмотра.)
2.  Если ускоритель обрабатывается обработчиком просмотра, его следует обработать и вернуть \_ ОК.
3.  Если ускоритель не обрабатывается обработчиком просмотра, Сравните сообщение с помощью функции [**Accelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) с полученной таблицей сочетаний клавиш.
4.  Если ускоритель соответствует записи в этой таблице сочетаний клавиш, вызовите [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) и возвратите результат.
5.  Если сочетание клавиш не соответствует ни одной записи в таблице сочетаний клавиш, возвращается \_ значение false.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler:: unload

При вызове этого метода следует прекратить обработку, освободить все ресурсы, выделенные с помощью считывания данных из потока, и освободить сам [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) .

После вызова этого метода обработчик должен быть повторно инициализирован перед любой попыткой вызова [**IPreviewHandler::D опревиев**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) .

## <a name="ipreviewhandlervisuals"></a>ипревиевхандлервисуалс

-   [Ипревиевхандлервисуалс:: Сетбаккграундколор](#ipreviewhandlervisualssetbackgroundcolor)
-   [Ипревиевхандлервисуалс:: Сетфонт](#ipreviewhandlervisualssetfont)
-   [Ипревиевхандлервисуалс:: Сеттекстколор](#ipreviewhandlervisualssettextcolor)

Эти методы должны быть реализованы, когда обработчик предварительного просмотра направляет ответ на схемы цвета и шрифта узла. Узел запрашивает обработчик для [**ипревиевхандлервисуалс**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals). Если обнаружена поддержка, узел предоставляет ему цвет, шрифт и цвет текста.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>Ипревиевхандлервисуалс:: Сетбаккграундколор

Сохраните этот цвет и используйте его при подготовке к просмотру, если требуется предоставить цвет фона. Например, для заполнения окна при визуализации обработчика в область, меньшую, чем область, предоставленная [**IPreviewHandler:: сетвиндов**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) и [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Однако обратите внимание, что не следует рисовать за пределами области, предоставляемой этими методами.

Если этот метод вызывается в то время, когда Предварительная версия уже готовится к просмотру, то отрисовку следует перезапустить с помощью этого цвета фона.

### <a name="ipreviewhandlervisualssetfont"></a>Ипревиевхандлервисуалс:: Сетфонт

Сохраняйте сведения о шрифтах и используйте их при подготовке к просмотру, если требуется отображать текст, согласованный с текущими параметрами Windows Vista.

### <a name="ipreviewhandlervisualssettextcolor"></a>Ипревиевхандлервисуалс:: Сеттекстколор

Сохраните эти сведения о цвете текста и используйте их во время подготовки к просмотру, если требуется отображать текст, согласованный с текущими параметрами Windows Vista.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обработчик предварительной версии и узел предварительной версии оболочки](preview-handlers.md)
</dt> <dt>

[Регистрация обработчика просмотра](how-to-register-a-preview-handler.md)
</dt> <dt>

[Рекомендации по обработчику предварительной версии](preview-handler-guidelines.md)
</dt> </dl>

 

 
