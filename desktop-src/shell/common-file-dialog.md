---
description: Начиная с Windows Vista, диалоговое окно общих элементов заменяет более старое общее диалоговое окно файла при использовании для открытия или сохранения файла.
title: Диалоговое окно общих элементов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342845"
---
# <a name="common-item-dialog"></a>Диалоговое окно общих элементов

Начиная с Windows Vista, диалоговое окно общих элементов заменяет более старое общее диалоговое окно файла при использовании для открытия или сохранения файла. Диалоговое окно Общие элементы используется в двух вариантах: диалоговое окно **Открыть** и диалоговое окно **сохранения** . Эти два диалоговых окна имеют большую часть их функциональных возможностей, но каждый из них имеет собственные уникальные методы.

Хотя эта новая версия называется диалоговым окном общих элементов, она по-своему по-своему часто называется общим диалоговым окном файла. Если вы не работаете исключительно с более старой версией Windows, следует предположить, что любое упоминание общего диалогового окна с файлом относится к этому диалоговому окну общих элементов.

Здесь обсуждаются следующие темы:

-   [Ифиледиалог, Ифилеопендиалог и Ифилесаведиалог](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Пример использования](#sample-usage)
-   [Прослушивание событий из диалогового окна](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [Оншаревиолатион и Оноверврите](#onshareviolation-and-onoverwrite)
-   [Настройка диалогового окна](#customizing-the-dialog)
    -   [Добавление параметров к кнопке «ОК»](#adding-options-to-the-ok-button)
    -   [Реагирование на события в добавленных элементах управления](#responding-to-events-in-added-controls)
-   [Полные примеры](#full-samples)
-   [См. также](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>Ифиледиалог, Ифилеопендиалог и Ифилесаведиалог

В Windows Vista реализованы диалоговые окна **открытия** и **сохранения** : CLSID \_ филеопендиалог и CLSID \_ филесаведиалог. Эти диалоговые окна показаны здесь.

![снимок экрана диалогового окна "Открыть"](images/cid/openfiledialog.png)

![снимок экрана — диалоговое окно "Сохранить как"](images/cid/savefiledialog.png)

[**Ифилеопендиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) и [**ифилесаведиалог**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) наследуют от [**ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) и используют большую часть их функциональных возможностей. Кроме того, диалоговое окно **Открыть** поддерживает **ифилеопендиалог**, а диалоговое окно **сохранения** поддерживает **ифилесаведиалог**.

Реализация общего элемента диалогового окна в Windows Vista предоставляет несколько преимуществ по сравнению с реализацией, реализованной в предыдущих версиях:

-   Поддерживает непосредственное использование пространства имен оболочки через [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) вместо использования путей файловой системы.
-   Включает простую настройку диалогового окна, например задание метки на кнопке « **ОК** » без необходимости выполнения процедуры обработчика.
-   Поддерживает более обширную настройку диалогового окна за счет добавления набора элементов управления, управляемых данными, которые работают без шаблона диалогового окна Win32. Эта схема настройки освобождает вызывающий процесс от макета пользовательского интерфейса. Поскольку любые изменения в разработке диалогового окна продолжают использовать эту модель данных, реализация диалогового окна не привязана к конкретной текущей версии диалогового окна.
-   Поддерживает уведомление вызывающего объекта о событиях в диалоговом окне, например изменение выбора или изменение типа файла. Также позволяет вызывающему процессу подключать определенные события в диалоговом окне, например синтаксический анализ.
-   В появились новые возможности диалогового окна, такие как добавление на панель **мест** определенных вызывающих объектов.
-   В диалоговом окне **сохранения** разработчики могут воспользоваться новыми функциями метаданных оболочки Windows Vista.

Кроме того, разработчики могут выбрать реализацию следующих интерфейсов:

-   [**Ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) для получения уведомлений о событиях в диалоговом окне.
-   [**Ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , чтобы добавить элементы управления в диалоговое окно.
-   [**Ифиледиалогконтролевентс**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) , чтобы получать уведомления о событиях в этих добавленных элементах управления.

Диалоговое окно **открытия** или **сохранения** возвращает объект [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) или [**ишеллитемаррай**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) в вызывающий процесс. Затем вызывающий может использовать отдельный объект **интерфейса IShellItem** для получения пути к файловой системе или для открытия потока на элементе для чтения или записи данных.

Флаги и параметры, доступные для новых методов диалогового окна, очень похожи на старые флаги **ОФН** , обнаруженные в структуре [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) и используемые в [**GetOpenFilename**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) и [**жетсавефиленаме**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Многие из них идентичны, за исключением того, что они начинаются с префикса Фос. Полный список можно найти в разделах [**ифиледиалог::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) Ифиледиалог и [**:: сетоптионс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) . Диалоговые окна **открытия** и **сохранения** создаются по умолчанию с самыми распространенными флагами. Для диалогового окна **Открыть** это (Фос \_ пасмустексист \| Фос \_ выполнить операцию filemustexist \| Фос \_ Ночанжедир) и для диалогового окна **сохранить** это (Фос овервритепромпт Фос \_ \| \_ нореадонлиретурн \| Фос пасмустексист FOS \_ \| \_ NOCHANGEDIR).

[**Ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) и его дочерние интерфейсы наследуют от и расширяют [**имодалвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). Параметр [**Показывать**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) принимает в качестве единственного параметра маркер родительского окна. Если функция **Показывать** успешно возвращает значение, имеется допустимый результат. Если он возвращает значение `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , это означает, что пользователь отменил диалоговое окно. Он также может вернуть другой код ошибки, например **E \_ OUTOFMEMORY**.

### <a name="sample-usage"></a>Пример использования

В следующих разделах показан пример кода для различных задач диалогового окна.

-   [Базовое использование](#basic-usage)
-   [Ограничение результатов для элементов файловой системы](#limiting-results-to-file-system-items)
-   [Указание типов файлов для диалогового окна](#specifying-file-types-for-a-dialog)
-   [Управление папкой по умолчанию](#controlling-the-default-folder)
-   [Добавление элементов на панель мест](#adding-items-to-the-places-bar)
-   [Сохраняемость состояния](#state-persistence)
-   [Возможности многовыборки](#multiselect-capabilities)

Большинство примеров кода можно найти в Windows SDK [общем файле](samples-commonfiledialog.md).

### <a name="basic-usage"></a>Основное использование

В следующем примере показано, как запустить **открытое** диалоговое окно. В этом примере он ограничен документами Microsoft Word.

> [!Note]  
> Несколько примеров в этом разделе используют `CDialogEventHandler_CreateInstance` вспомогательную функцию для создания экземпляра реализации [**ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) . Чтобы использовать эту функцию в собственном коде, скопируйте исходный код `CDialogEventHandler_CreateInstance` функции из [общего файлового диалога](samples-commonfiledialog.md), из которого берутся все примеры в этом разделе.

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a>Ограничение результатов для элементов файловой системы

В следующем примере, взятом из выше, показано, как ограничить результаты для элементов файловой системы. Обратите внимание, что [**ифиледиалог:: сетоптионс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) добавляет новый флаг к значению, полученному с помощью [**ифиледиалог::-Options**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions). Рекомендуем использовать этот метод.


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a>Указание типов файлов для диалогового окна

Чтобы задать определенные типы файлов, которые диалоговое окно может обработано, используйте метод [**ифиледиалог:: сетфилетипес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) . Этот метод принимает массив структур [**комдлг \_ филтерспек**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , каждый из которых представляет тип файла.

Механизм расширения по умолчанию в диалоговом окне не изменился с [**GetOpenFilename**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) и [**жетсавефиленаме**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Расширение имени файла, добавляемое к тексту, которое пользователь вводит в поле ввода имени файла, инициализируется при открытии диалогового окна. Он должен соответствовать типу файла по умолчанию (который был выбран при открытии диалогового окна). Если тип файла по умолчанию — " \* . \* " (все файлы) файл может быть расширением по своему усмотрению. Если пользователь выбирает другой тип файла, расширение автоматически обновляет первое расширение имени файла, связанное с этим типом файлов. Если пользователь выбирает " \* . \* " (все файлы), расширение возвращается к исходному значению.

В следующем примере показано, как это было сделано ранее.


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a>Управление папкой по умолчанию

Почти любую папку в пространстве имен Shell можно использовать в качестве папки по умолчанию для диалогового окна (папки, представленной при открытии или сохранении файла пользователем). Вызовите метод [**ифиледиалог:: сетдефаултфолдер**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) перед вызовом метода [**демонстрация**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) .

Папка по умолчанию — это папка, в которой диалоговое окно запускается при первом его открытии пользователем из приложения. После этого диалоговое окно откроется в последней папке, открытой пользователем, или в последней папке, используемой для сохранения элемента. Дополнительные сведения см. в разделе [Сохранение состояния](#state-persistence) .

Можно заставить диалоговое окно всегда отображать ту же папку при открытии, вне зависимости от предыдущего действия пользователя, вызывая [**ифиледиалог:: сетфолдер**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder). Однако делать это не рекомендуется. Если вызвать **сетфолдер** перед отображением диалогового окна, то Последнее расположение, которое пользователь сохранил или открыл из, не отображается. Если для этого поведения нет особой причины, это не является хорошим или ожидаемым пользовательским интерфейсом, и его следует избегать. В большинстве случаев метод [**ифиледиалог:: сетдефаултфолдер**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) является лучшим методом.

При первом сохранении документа в диалоговом окне **сохранения** необходимо следовать тем же рекомендациям, что и при определении исходной папки, как это делалось в диалоговом окне **Открыть** . Если пользователь редактирует ранее существующий документ, откройте диалоговое окно в папке, в которой хранится этот документ, и заполните поле ввода именем этого документа. Вызовите [**ифилесаведиалог:: сетсавеаситем**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) с текущим элементом до вызова метода [**демонстрации**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).

### <a name="adding-items-to-the-places-bar"></a>Добавление элементов на панель мест

В следующем примере показано добавление элементов на панель **мест** .


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a>Сохраняемость состояния

До Windows Vista состояние, например Последнее посещение папки, было сохранено отдельно для каждого процесса. Однако эта информация использовалась независимо от конкретного действия. Например, приложение для редактирования видео будет представлять ту же папку в диалоговом окне « **рендеринг как** », что и в диалоговом окне « **Импорт носителя** ». В Windows Vista можно использовать более конкретные идентификаторы GUID. Чтобы назначить **идентификатор GUID** для диалогового окна, вызовите метод [**Ифиледиалог:: сетклиентгуид**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>Возможности многовыборки

Функциональные возможности, доступные в диалоговом окне **Открыть** , можно получить с [**помощью метода,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) как показано ниже.


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a>Прослушивание событий из диалогового окна

Вызывающий процесс может зарегистрировать интерфейс [**ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) в диалоговом окне с помощью методов [**Ифиледиалог:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) и [**ифиледиалог:: unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) , как показано здесь.

Это взято из примера [использования Basic](#basic-usage) .


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



Основная часть обработки диалогового окна будет помещена здесь.


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



Вызывающий процесс может использовать события для уведомления о том, что пользователь изменяет папку, тип файла или выделенный фрагмент. Эти события особенно полезны, когда вызывающий процесс добавил элементы управления в диалоговое окно (см. раздел [Настройка диалогового окна](#customizing-the-dialog)) и должен изменить состояние этих элементов управления в реакцию на эти события. Полезным во всех случаях является способность вызывающего процесса предоставлять пользовательский код для решения таких ситуаций, как нарушения совместного доступа, перезапись файлов или определение допустимости файла перед закрытием диалогового окна. Некоторые из этих случаев описаны в этом разделе.

### <a name="onfileok"></a>OnFileOk

Этот метод вызывается после того, как пользователь выберет элемент, непосредственно перед закрытием диалогового окна. После закрытия диалогового окна приложение может вызвать [**ифиледиалог::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) или [**ифилеопендиалог:: unresults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) . Если выбранный элемент приемлем, он может вернуть S \_ ОК. В противном случае они возвращают \_ false и экранный интерфейс, сообщающий пользователю о том, почему выбранный элемент является недопустимым. Если \_ возвращается значение S false, диалоговое окно не закрывается.

Вызывающий процесс может использовать маркер окна самого диалогового окна в качестве родительского элемента пользовательского интерфейса. Этот маркер можно получить при первом вызове [**иолевиндов:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , а затем вызвать [**иолевиндов::**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) с маркером, как показано в этом примере.


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a>Оншаревиолатион и Оноверврите

Если пользователь выбирает перезапись файла в диалоговом окне **сохранения** или если файл, который требуется сохранить или заменить, используется и не может быть записан в (нарушение общего доступа), приложение может предоставить пользовательские функции для переопределения поведения диалогового окна по умолчанию. По умолчанию при перезаписи файла в диалоговом окне отображается запрос, позволяющий пользователю проверить это действие. В случае нарушения общего доступа по умолчанию в диалоговом окне отображается сообщение об ошибке, оно не закрывается и пользователь должен выбрать другой вариант. Вызывающий процесс может переопределить эти значения по умолчанию и при необходимости отобразить собственный пользовательский интерфейс. В диалоговом окне можно указать отказаться от файла и оставить открытым или принять его и закрыть его успешно.

## <a name="customizing-the-dialog"></a>Настройка диалогового окна

В диалоговое окно можно добавить множество элементов управления без указания шаблона диалогового окна Win32. К этим элементам управления относятся кнопка, ComboBox, EditBox, Чеккбуттон, списки RadioButton, группы, разделители и статические текстовые элементы управления. Вызовите **QueryInterface** для объекта диалогового окна ([**ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**ифилеопендиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)или [**ифилесаведиалог**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)), чтобы получить указатель [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) . Используйте этот интерфейс для добавления элементов управления. Каждый элемент управления имеет связанный идентификатор, предоставленный вызывающим объектом, а также *видимое* и *включенное* состояние, которое может быть задано вызывающим процессом. С некоторыми элементами управления, такими как кнопка, также связан текст.

В «визуальную группу» можно добавить несколько элементов управления, которые перемещаются в виде одного элемента в макете диалогового окна. С группами может быть связана метка.

Элементы управления можно добавлять только до отображения диалогового окна. Однако после отображения диалогового окна элементы управления могут быть скрыты или отображены по желанию, возможно, в ответ на действия пользователя. В следующих примерах показано, как добавить список переключателей в диалоговое окно.


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a>Добавление параметров к кнопке «ОК»

Аналогичным образом можно добавлять варианты к кнопкам **Открыть** или **сохранить** , которые являются кнопкой **ОК** для соответствующих типов диалоговых окон. Доступ к параметрам можно получить с помощью раскрывающегося списка, присоединенного к кнопке. Первый элемент в списке преобразуется в текст кнопки. В следующем примере показано, как предоставить кнопку " **Открыть** " с двумя возможностями: "Открыть" и "открыть только для чтения".


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





Выбранный пользователь может быть проверен после того, как диалоговое окно будет возвращено из метода [**показа**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) , как для поля со списком, или проверяться в ходе обработки с помощью [**Ифиледиаложевентс:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).

### <a name="responding-to-events-in-added-controls"></a>Реагирование на события в добавленных элементах управления

Обработчик событий, предоставляемый вызывающим процессом, может реализовать [**ифиледиалогконтролевентс**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) в дополнение к [**ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents). **Ифиледиалогконтролевентс** позволяет вызывающему процессу реагировать на эти события:

-   Кнопка нажата
-   Изменено состояние Чеккбуттон
-   Элемент, выбранный из списка меню, ComboBox или RadioButton
-   Управление активацией. Он отправляется, когда меню собирается отобразить раскрывающийся список, если вызывающий процесс хочет изменить элементы в списке.

## <a name="full-samples"></a>Полные примеры

Ниже приведены полные, загружаемые образцы C++ из пакета средств разработки программного обеспечения (SDK) для Windows, демонстрирующие использование и взаимодействие с диалоговым окном общих элементов.

-   [Пример: стандартное диалоговое окно выбора файла](samples-commonfiledialog.md)
-   [Пример: режимы стандартного диалогового окна выбора файла](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IID \_ ППВ \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
