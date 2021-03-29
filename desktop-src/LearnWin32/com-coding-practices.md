---
title: Методики программирования COM
description: В этом разделе описываются способы повышения эффективности и надежности кода COM.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104134711"
---
# <a name="com-coding-practices"></a>Методики программирования COM

В этом разделе описываются способы повышения эффективности и надежности кода COM.

-   [\_ \_ Оператор ууидоф](/windows)
-   [Макрос IID \_ ППВ \_ args](/windows)
-   [Шаблон Саферелеасе](#the-saferelease-pattern)
-   [Интеллектуальные указатели COM](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>\_ \_ Оператор ууидоф

При сборке программы могут возникать ошибки компоновщика, аналогичные следующим:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Эта ошибка означает, что константа GUID была объявлена с внешней компоновкой (**extern**), и компоновщику не удалось найти определение константы. Значение константы GUID обычно экспортируется из файла статической библиотеки. При использовании Microsoft Visual C++ можно избежать необходимости связывать статическую библиотеку с помощью оператора **\_ \_ ууидоф** . Этот оператор является расширением языка Майкрософт. Он возвращает значение идентификатора GUID из выражения. Выражение может быть именем типа интерфейса, именем класса или указателем интерфейса. С помощью **\_ \_ ууидоф** можно создать объект диалогового окна общего элемента следующим образом:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



Компилятор извлекает значение идентификатора GUID из заголовка, поэтому экспорт библиотеки не требуется.

> [!Note]  
> Значение идентификатора GUID связывается с именем типа путем объявления `__declspec(uuid( ... ))` в заголовке. Дополнительные сведения см. в документации по **\_ \_ declspec** в документации по Visual C++.

 

## <a name="the-iid_ppv_args-macro"></a>Макрос IID \_ ППВ \_ args

Мы видели, что методы [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) и [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) нуждаются в преобразовании финального параметра в **тип \* \* void** . Это создает потенциал для несоответствия типов. Рассмотрим следующий фрагмент кода:


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



Этот код запрашивает интерфейс [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , но передается в указатель [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Выражение **\_ приведения переинтерпретации** обходит систему типов C++, поэтому компилятор не будет перехватывать эту ошибку. В лучшем случае, если объект не реализует запрошенный интерфейс, вызов просто завершается ошибкой. В худшем случае функция выполняется успешно и имеется несовпадающий указатель. Иными словами, тип указателя не соответствует фактической таблице vtable в памяти. Как можно себе представить, на этом этапе ничего не может произойти.

> [!Note]  
> Таблица виртуальных методов ( *vtable* ) — это таблица указателей на функции. Таблица vtable заключается в том, как COM привязывает вызов метода к его реализации во время выполнения. Некстати, таблицы vtable — это то, как большинство компиляторов C++ реализуют виртуальные методы.

 

Макрос [**IID \_ ППВ \_ argss**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) помогает избежать этого класса ошибки. Чтобы использовать этот макрос, замените следующий код:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



следующим кодом:


```C++
IID_PPV_ARGS(&pFileOpen)
```



Макрос автоматически вставляет `__uuidof(IFileOpenDialog)` идентификатор интерфейса, поэтому он гарантированно соответствует типу указателя. Ниже приведен измененный (и правильный) код.


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Один и тот же макрос можно использовать с [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>Шаблон Саферелеасе

Подсчет ссылок — это одна из тех вещей в программировании, которая, по сути, проста, но она также утомительна, что позволяет легко получить ошибку. Типовые ошибки включают:

-   Не удается освободить указатель интерфейса по завершении его использования. Этот класс ошибок приведет к утечке памяти программой и другим ресурсам, так как объекты не уничтожаются.
-   Вызов [**выпуска**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с недопустимым указателем. Например, эта ошибка может произойти, если объект не был создан. Эта категория ошибок, вероятно, приведет к сбою программы.
-   Разыменование указателя интерфейса после вызова метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) . Эта ошибка может привести к сбою программы. Что еще хуже, это может привести к сбою программы в случайном будущем, что затрудняет отслеживание исходной ошибки.

Одним из способов избежать этих ошибок является вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с помощью функции, которая безопасно освобождает указатель. В следующем коде показана функция, которая делает следующее:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



Эта функция принимает указатель COM-интерфейса в качестве параметра и выполняет следующие действия:

1.  Проверяет, имеет ли указатель **значение NULL**.
2.  Вызывает метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , если указатель не имеет **значение NULL**.
3.  Устанавливает указатель на **значение NULL**.

Ниже приведен пример использования `SafeRelease` :


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



Если [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) выполнен, вызов `SafeRelease` освобождает указатель. Если **CoCreateInstance** завершается ошибкой, *пфилеопен* остается **пустым**. `SafeRelease`Функция проверяет наличие этого и пропускает вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

Также можно вызвать `SafeRelease` более одного раза в одном и том же указателе, как показано ниже:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Интеллектуальные указатели COM

`SafeRelease`Функция полезна, но требует запоминать две вещи:

-   Инициализируйте каждый указатель интерфейса на **значение NULL**.
-   Вызовите, `SafeRelease` прежде чем каждый указатель выходит за пределы области.

Как программист на C++, вы, вероятно, думаете, что вам не нужно запоминать ни одно из этих вещей. В конце концов, вот почему C++ имеет конструкторы и деструкторы. Было бы неплохо иметь класс, который заключает указатель базового интерфейса и автоматически инициализирует и освобождает указатель. Другими словами, нам нужно нечто вроде этого:


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



Приведенное здесь определение класса является неполным и не может использоваться, как показано. Как минимум необходимо определить конструктор копии, оператор присваивания и способ доступа к базовому указателю COM. К счастью, вам не нужно выполнять какую-либо из этих действий, поскольку Microsoft Visual Studio уже предоставляет класс интеллектуального указателя как часть библиотеки ATL.

Класс интеллектуального указателя ATL называется **CComPtr**. (Существует также класс **CComQIPtr** , который здесь не рассматривается.) Ниже приведен пример [открытого диалогового окна](example--the-open-dialog-box.md) , в котором используется **CComPtr**.


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



Основное различие между этим кодом и исходным примером состоит в том, что эта версия не вызывает явно [**выпуск**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Когда экземпляр **CComPtr** выходит за пределы области действия, деструктор вызывает метод **Release** в базовом указателе.

**CComPtr** — это шаблон класса. Аргумент шаблона является типом COM-интерфейса. Внутри **CComPtr** содержит указатель этого типа. **CComPtr** переопределяет **оператор-> ()** и **оператор& ()** , чтобы класс действовал как базовый указатель. Например, следующий код эквивалентен вызову метода **ифилеопендиалог::** reby напрямую:


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** также определяет метод **CComPtr:: CoCreateInstance** , который вызывает функцию COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с некоторыми значениями параметров по умолчанию. Единственным обязательным параметром является идентификатор класса, как показано в следующем примере:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



Метод **CComPtr:: CoCreateInstance** предоставляется исключительно в качестве удобства; При желании можно по-прежнему вызывать функцию COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="next"></a>Следующая

[Обработка ошибок в COM](error-handling-in-com.md)

 

 