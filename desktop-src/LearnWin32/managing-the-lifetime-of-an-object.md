---
title: Управление жизненным циклом объекта
description: Узнайте, как управлять жизненным циклом объекта с помощью методов AddRef и Release.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550459"
---
# <a name="managing-the-lifetime-of-an-object"></a>Управление жизненным циклом объекта

Существует правило для COM-интерфейсов, которые еще не упоминались. Каждый COM-интерфейс должен напрямую или косвенно наследовать от интерфейса с именем [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Этот интерфейс предоставляет некоторые базовые возможности, которые должны поддерживаться всеми COM-объектами.

Интерфейс [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) определяет три метода:

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

Метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) позволяет программе запрашивать возможности объекта во время выполнения. Мы будем говорить подробнее об этом в следующем разделе, [запросив объект для интерфейса](asking-an-object-for-an-interface.md). Методы [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) используются для управления временем существования объекта. Это тема этого раздела.

## <a name="reference-counting"></a>Подсчет ссылок

Независимо от того, что может сделать программа, в некоторый момент она будет распределять и освобождать ресурсы. Выделить ресурс несложно. Знание того, когда следует освобождать ресурс, очень сложно, особенно если время существования ресурса выходит за пределы текущей области. Эта проблема не является уникальной для COM. Любая программа, выделяющая память кучи, должна решить эту же проблему. Например, в C++ используются автоматические деструкторы, в то время как C# и Java используют сборку мусора. COM использует подход, называемый *подсчетом ссылок*.

Каждый COM-объект поддерживает внутреннее число. Это называется счетчиком ссылок. Счетчик ссылок отслеживает, сколько ссылок на объект активно в данный момент. Когда число ссылок становится равным нулю, объект удаляет себя. Последняя часть стоит повторять: объект удаляет себя. Программа никогда не удаляет объект явным образом.

Ниже приведены правила для подсчета ссылок.

-   При первом создании объекта его счетчик ссылок равен 1. На этом этапе программа имеет один указатель на объект.
-   Программа может создать новую ссылку путем дублирования (копирования) указателя. При копировании указателя необходимо вызвать метод [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) объекта. Этот метод увеличивает значение счетчика ссылок на единицу.
-   По завершении использования указателя на объект необходимо вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Метод **Release** уменьшает значение счетчика ссылок на единицу. Он также сделает указатель недействительным. Не используйте указатель снова после вызова **Release**. (При наличии других указателей на один и тот же объект можно продолжать использовать эти указатели.)
-   При вызове [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с каждым указателем число ссылок на объект достигает нуля, а сам объект удаляет себя.

На следующей диаграмме показан простой, но типичный вариант.

![Схема, на которой показан простой вариант подсчета ссылок.](images/com04.png)

Программа создает объект и сохраняет указатель (*p*) в объекте. На этом этапе счетчик ссылок равен 1. Когда программа завершает работу с указателем, она вызывает [**выпуск**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release). Счетчик ссылок уменьшается до нуля, и объект удаляет себя. Now *p* недопустимо. Использование *p* для дальнейших вызовов методов является ошибкой.

На следующей схеме показан более сложный пример.

![Иллюстрация, показывающая подсчет ссылок](images/com05.png)

Здесь программа создает объект и сохраняет указатель *p*, как и раньше. Затем программа копирует *p* в новую переменную, *q*. На этом этапе программа должна вызывать [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) для увеличения числа ссылок. Теперь число ссылок равно 2, и в объекте есть два допустимых указателя. Теперь предположим, что программа завершена с использованием *p*. Программа вызывает [**выпуск**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), счетчик ссылок переходит в 1, а *p* больше не действует. Однако *q* остается действительным. Позже программа завершит использование *q*. Поэтому он снова вызывает метод **Release** . Число ссылок становится равным нулю, а объект удаляет себя.

Может возникнуть вопрос, почему программа скопирует *p*. Есть две основные причины: сначала может потребоваться сохранить указатель в структуре данных, например в списке. Во вторых, может потребоваться, чтобы указатель оставался за пределами текущей области исходной переменной. Поэтому его нужно скопировать в новую переменную с более широкими областями.

Одним из преимуществ подсчета ссылок является то, что вы можете совместно использовать указатели в разных разделах кода, не используя разные пути кода для удаления объекта. Вместо этого каждый путь кода просто вызывает метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , когда этот путь кода выполняется с помощью объекта. Объект обрабатывает сам себя в нужное время.

## <a name="example"></a>Пример

Ниже приведен код из [примера открытия диалогового окна](example--the-open-dialog-box.md) .

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

Подсчет ссылок выполняется в двух местах этого кода. Во первых, если программа успешно создает объект диалогового окна общего элемента, он должен вызвать [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) для указателя *пфилеопен* .

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

Во-вторых, [**когда метод**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) возвращает указатель на интерфейс, программа должна вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) для указателя *питем* .

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Обратите внимание, что в обоих случаях вызов [**выпуска**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) является последним, который происходит перед тем, как указатель выходит из области действия. Также обратите внимание, что метод **Release** вызывается только после проверки **значения HRESULT** на успешное выполнение. Например, если вызов [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) завершается ошибкой, то указатель *пфилеопен* является недопустимым. Поэтому вызов метода **Release** с указателем будет ошибкой.

## <a name="next"></a>Следующая

[Запрос объекта для интерфейса](asking-an-object-for-an-interface.md)