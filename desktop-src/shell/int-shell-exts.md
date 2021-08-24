---
description: Большая часть реализации объекта обработчика расширений оболочки определяется его типом. Однако есть некоторые распространенные элементы. В этом разделе обсуждаются аспекты реализации, совместно используемые всеми обработчиками расширений оболочки.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Инициализация обработчиков расширений оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f83a47400cff5d0fa4628f6f6f9d9ba74b158947c7843f61831d54f62c7a6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661224"
---
# <a name="initializing-shell-extension-handlers"></a>Инициализация обработчиков расширений оболочки

Большая часть реализации объекта обработчика расширений оболочки определяется его типом. Однако есть некоторые распространенные элементы. В этом разделе обсуждаются аспекты реализации, совместно используемые всеми обработчиками расширений оболочки.

Все обработчики расширений оболочки — это объекты модели COM. Им необходимо назначить идентификатор GUID и зарегистрировать, как описано в разделе [Регистрация обработчиков расширений оболочки](handlers.md). Они реализуются в виде библиотек DLL и должны экспортировать следующие стандартные функции:

-   [**DllMain**](../dlls/dllmain.md). Стандартная точка входа для библиотеки DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Предоставляет фабрику класса объекта.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM вызывает эту функцию, чтобы определить, обслуживает ли объект какие-либо клиенты. В противном случае система может выгрузить библиотеку DLL и освободить связанную с ней память.

Как и все COM-объекты, обработчики расширений оболочки должны реализовывать интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и [фабрику классов](../com/implementing-iclassfactory.md). большинство из них также должны реализовывать интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) или [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) в Windows XP или более ранней версии. они были заменены на [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) и [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) в Windows Vista. Оболочка использует эти интерфейсы для инициализации обработчика.

Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) должен быть реализован следующим образом:

-   Обработчики значков
-   Обработчики данных
-   Удалить обработчики

Интерфейс [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) должен быть реализован следующим образом:

-   Обработчики контекстного меню
-   Обработчики перетаскивания
-   Обработчики страницы свойств

В оставшейся части этого раздела обсуждаются следующие темы:

-   [Реализация IPersistFile](#implementing-ipersistfile)
-   [Реализация Ишеллекстинит](#implementing-ishellextinit)
-   [Настройка всплывающей подсказки](#infotip-customization)
-   [Связанные темы](#related-topics)

## <a name="implementing-ipersistfile"></a>Реализация IPersistFile

Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) предназначен для того, чтобы объект был загружен или сохранен в файл на диске. В нем есть шесть методов в дополнение к [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), пять его собственных и методу [**ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , который он наследует от [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). С помощью расширений оболочки **IPersist** используется только для инициализации объекта обработчика расширений оболочки. Так как обычно нет необходимости выполнять чтение или запись на диск, только для методов **класса** и метода [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) требуется только реализация без маркера.

Оболочка вызывает метод [**ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , а функция возвращает идентификатор класса (CLSID) объекта обработчика расширений. Затем оболочка вызывает [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) и передает два значения. Первая, *псзфиле*, представляет собой строку в Юникоде с именем файла или папки, в которой будет выполняться оболочка. Второй — *двмоде*, который указывает режим доступа к файлу. Так как обычно нет необходимости в доступе к файлам, *двмоде* обычно равен нулю. Метод сохраняет эти значения в соответствии с последующими ссылками.

В следующем фрагменте кода показано, как типичный обработчик расширений оболочки реализует методы класса [**и метода-**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) [**ClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) . Он предназначен для работы с ANSI или Unicode. CLSID \_ сампликссандлер — это идентификатор GUID объекта обработчика расширений, а ксамплешеллекстенсион — имя класса, используемого для реализации интерфейса. Переменные **m \_ сзфиленаме** и **m \_ двмоде** являются частными переменными, которые используются для хранения имени файла и флагов доступа.


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>Реализация Ишеллекстинит

Помимо [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), в интерфейсе [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) имеется только один метод, [**ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Метод имеет три параметра, которые оболочка может использовать для передачи различных типов данных. Передаваемые значения зависят от типа обработчика, а некоторые могут иметь значение **null**.

-   *пидлфолдер* содержит указатель папки на список идентификаторов элементов (Пидл). Это абсолютно ПИДЛ. Для расширений таблицы свойств это значение равно **null**. Для расширений контекстного меню это ПИДЛ папки, содержащей элемент, контекстное меню которого отображается. Для обработчиков перетаскивания, не заданных по умолчанию, это ПИДЛ целевой папки.
-   *pDataObject* содержит указатель на интерфейс [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) объекта данных. Объект данных содержит одно или несколько имен файлов в формате [CF \_ HDROP](dragdrop.md) .
-   *хрегкэй* содержит раздел реестра для объекта File или типа Folder.

Метод [**ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) сохраняет имя файла, указатель [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) и раздел реестра, необходимые для последующего использования. В следующем фрагменте кода показана реализация **ишеллекстинит:: Initialize**. Для простоты в этом примере предполагается, что объект данных содержит только один файл. Как правило, объект данных может содержать несколько файлов, каждый из которых необходимо извлечь.


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>Настройка всплывающей подсказки

Существует два способа настройки инфотипс. Один из способов — реализовать объект, который поддерживает [**икуеринфо**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) , а затем зарегистрировать объект в соответствующем подразделе реестра (см. ниже). Кроме того, можно указать либо фиксированную строку, либо список некоторых свойств файла для отображения.

Чтобы отобразить фиксированную строку для расширения пространства имен, создайте подраздел с именем **подсказки** под ключом CLSID расширения пространства имен. Установите данные этого подраздела в качестве строки, которую необходимо отобразить.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Чтобы отобразить фиксированную строку для типа файла, создайте подраздел с именем **подсказки** под ключом **ProgID** для типа файла, для которого вы хотите предоставить инфотипс. Установите данные этого подраздела в качестве строки, которую необходимо отобразить.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Если требуется, чтобы оболочка отображала определенные свойства файла в подсказке для конкретного типа файлов, создайте **подсказку** под ключом **ProgID** для этого типа файлов. Установите данные этого подраздела в виде разделенного точкой с запятой списка канонических имен свойств или {fmtid}, пар PID, где *пропнаме* является каноническим именем свойства и *{fmtid}, PID* — это [**пара fmtid/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Можно использовать следующие имена свойств.



| Имя свойства    | Описание                   | Получено из                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Автор           | Автор документа        | [**\_Автор пидси**](../stg/the-summary-information-property-set.md)                             |
| Название            | Название документа         | [**\_заголовок пидси**](../stg/the-summary-information-property-set.md)                              |
| Тема          | Сводка по теме               | [**\_Тема пидси**](../stg/the-summary-information-property-set.md)                            |
| Комментировать          | Комментарии к документу             | [**Пидси \_ Свойства комментария**](../stg/the-summary-information-property-set.md) или папки/диска |
| PageCount        | Количество страниц               | [**ПИДСИ \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                          |
| Имя             | Понятное имя                 | Стандартное представление папки                                                                      |
| оригиналлокатион | Расположение исходного файла     | Папка "портфель" и папка "Корзина"                                                   |
| датеделетед      | Файл даты удален         | Папка корзины                                                                        |
| Тип             | Тип файла                  | Представление сведений о стандартной папке                                                              |
| Размер             | Размер файла                  | Представление сведений о стандартной папке                                                              |
| синккопин       | То же, что и Оригиналлокатион      | То же, что и Оригиналлокатион                                                                  |
| Изменен         | Дата последнего изменения            | Представление сведений о стандартной папке                                                              |
| Создание          | Дата создания                  | Представление сведений о стандартной папке                                                              |
| Обращения         | Дата последнего доступа            | Представление сведений о стандартной папке                                                              |
| Папка         | Каталог, содержащий файл | Результаты поиска документов                                                                   |
| Рейтинг             | Соответствие качества поиска       | Результаты поиска документов                                                                   |
| FreeSpace        | Доступное дисковое пространство       | Диски                                                                               |
| NumberOfVisits   | Количество посещений              | Папка "Избранное"                                                                          |
| Атрибуты       | Атрибуты файла               | Представление сведений о стандартной папке                                                              |
| Company          | Название компании                  | [**\_компания пиддси**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Категория         | Категория документа             | [**\_Категория пиддси**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Авторские права на мультимедиа               | [**ПИДМСИ \_ авторские права**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| хтмлинфотипфиле  | Файл всплывающей подсказки HTML             | Файл Desktop.ini для папки                                                               |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация обработчиков расширений оболочки](reg-shell-exts.md)
</dt> </dl>

 

 
