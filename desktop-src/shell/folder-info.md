---
description: В разделе Получение идентификатора папки обсуждаются два подхода к получению указателя объекта пространства имен на список идентификаторов элементов (ПИДЛ).
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: Получение сведений о содержимом папки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997210"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>Получение сведений о содержимом папки

В разделе [Получение идентификатора папки](folder-id.md) обсуждаются два подхода к получению указателя объекта пространства имен на список идентификаторов элементов (Пидл). Один из очевидных вопросов: когда у вас есть ПИДЛ, что можно делать с ним? Связанный вопрос: что делать, если ни один из подходов не работает или подходит для вашего приложения? Ответ на оба вопроса требует более подробного взгляда на то, как реализуется пространство имен. Ключом является интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

-   [Использование интерфейса Ишеллфолдер](#using-the-ishellfolder-interface)
-   [Перечисление содержимого папки](#enumerating-the-contents-of-a-folder)
-   [Определение отображаемых имен и других свойств](#determining-display-names-and-other-properties)
-   [Получение указателя на интерфейс Ишеллфолдер вложенной папки](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [Определение родительской папки объекта](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>Использование интерфейса Ишеллфолдер

Ранее в этой документации папки пространства имен назывались объектами. Хотя в этот момент термин использовался в слабом смысле, на самом деле это верно и в строгом смысле. Каждая папка пространства имен представлена объектом модели COM. Каждый объект Folder предоставляет ряд интерфейсов, которые можно использовать для самых разных задач. Некоторые интерфейсы, которые являются необязательными, могут не предоставляться всеми папками. Однако все папки должны предоставлять фундаментальный интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).

Первым шагом при использовании объекта Folder является получение указателя на его интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Помимо предоставления доступа к другим интерфейсам объекта, **ишеллфолдер** предоставляет группу методов, обрабатывающих ряд общих задач, некоторые из которых обсуждаются в этом разделе.

Чтобы получить указатель на интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) объекта пространства имен, необходимо сначала вызвать [**шжетдесктопфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder). Эта функция возвращает указатель на интерфейс **ишеллфолдер** корня пространства имен, рабочего стола. Когда у вас есть интерфейс **ишеллфолдер** рабочего стола, существует множество способов продолжения.

Если у вас уже есть ПИДЛ интересующей вас папки — например, путем вызова [**шжетфолдерлокатион**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)— вы можете извлечь его интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) , вызвав метод [**ишеллфолдер:: биндтубжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) рабочего стола. Если у вас есть путь к объекту файловой системы, необходимо сначала получить его ПИДЛ, вызвав метод [**ишеллфолдер::P арседисплайнаме**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) рабочего стола, а затем вызвать **Ишеллфолдер:: биндтубжект**. Если ни один из этих подходов не применим, можно использовать другие методы **ишеллфолдер** для навигации по пространству имен. Дополнительные сведения см. [в разделе Навигация по пространству имен](navigate.md).

## <a name="enumerating-the-contents-of-a-folder"></a>Перечисление содержимого папки

Первое, что обычно нужно сделать с папкой, — узнать, что она содержит. Сначала необходимо вызвать метод [**ишеллфолдер:: енумобжектс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) папки. Папка создаст стандартный объект перечисления OLE и возвратит его интерфейс [**иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) . Этот интерфейс предоставляет четыре стандартных метода:[**клонирование**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone), [**следующий**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next), [**Сброс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)и [**пропуск**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)—, которые можно использовать для перечисления содержимого папки.

Базовая процедура перечисления содержимого папки:

1.  Вызовите метод Folders [**ишеллфолдер:: енумобжектс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) , чтобы получить указатель на интерфейс [**иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) объекта перечисления.
2.  Передайте нераспределенный ПИДЛ в [**иенумидлист:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). **Далее** необходимо выделить Пидл, но приложение должно освободить его, когда оно больше не требуется. При **следующем** возврате Пидл будет содержать только идентификатор элемента объекта и завершающие символы **null** . Иными словами, это одноуровневая ПИДЛ, относительная для папки, а не полный ПИДЛ.
3.  Повторите шаг 2 до [**следующего**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) возврата значения \_ false, чтобы указать, что были перечислены все элементы.
4.  Вызовите метод **иенумидлист:: Release** , чтобы освободить объект перечисления.

> [!Note]  
> Важно отследить, работаете ли вы с полным или относительным ПИДЛ. Некоторые функции и методы принимают значение, но другие принимают только одну или другую.

 

Оставшиеся три метода [**иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) ([**Сброс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset), [**пропуск**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)и [**клонирование**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) полезны, если необходимо выполнить повторяющиеся перечисления папки. Они позволяют сбрасывать перечисление, пропускать один или несколько объектов и создавать копию объекта перечисления для сохранения его состояния.

## <a name="determining-display-names-and-other-properties"></a>Определение отображаемых имен и других свойств

После перечисления всех PIDL, содержащихся в папке, можно узнать, какие объекты они представляют. Интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) предоставляет ряд полезных методов, два из которых обсуждаются здесь. Другие методы **ишеллфолдер** и другие интерфейсы папок оболочки обсуждаются далее.

Одним из наиболее полезных свойств является отображаемое имя объекта. Чтобы получить отображаемое имя объекта, передайте его ПИДЛ в [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Хотя объект может находиться в любом месте под родительской папкой в пространстве имен, его ПИДЛ должен быть указан относительно папки.

[**Ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) Возвращает отображаемое имя как часть структуры [**стррет**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Поскольку извлечение отображаемого имени из структуры **стррет** может быть немного сложным, оболочка предоставляет две функции, которые выполняют задание, [**стрреттостр**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) и [**стрреттобуф**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa). Обе функции принимают структуру **стррет** и возвращают отображаемое имя как обычную строку. Они отличаются только тем, как выделяется строка.

В дополнение к отображаемому имени объект может иметь ряд атрибутов, например, является ли он папкой или может ли он быть перемещен. Атрибуты объекта можно получить, передав его ПИДЛ в [**ишеллфолдер:: жетаттрибутесоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof). Полный список атрибутов довольно большой, поэтому вы увидите ссылку для получения дополнительных сведений. Обратите внимание, что ПИДЛ, передаваемый в **жетаттрибутесоф** , должны быть одноуровневые. В частности, **ишеллфолдер:: жетаттрибутесоф** будет принимать PIDL, возвращаемый [**Иенумидлист:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). Можно передать массив PIDL, и **жетаттрибутесоф** будет возвращать эти атрибуты, которые все объекты в массиве являются общими.

При наличии полного пути или ПИДЛ объекта [**шжетфилеинфо**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) предоставляет простой способ получения сведений о объекте, который достаточно для многих целей. **Шжетфилеинфо** принимает полный путь или Пидл и возвращает разнообразные сведения об объекте, включая:

-   Отображаемое имя объекта
-   Атрибуты объекта
-   Дескрипторы значков объекта
-   Маркер списка системных образов
-   Путь к файлу, содержащему значок объекта

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>Получение указателя на интерфейс Ишеллфолдер вложенной папки

Чтобы определить, содержит ли ваша папка вложенные папки, вызовите [**ишеллфолдер:: жетаттрибутесоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) и проверьте, \_ установлен ли флаг папки сфгао. Если объект является папкой, можно выполнить привязку к нему, что дает указатель на его интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Чтобы выполнить привязку к вложенной папке, вызовите метод [**ишеллфолдер:: биндтубжект**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) родительской папки. Этот метод принимает ПИДЛ вложенной папки и возвращает указатель на его интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Получив этот указатель, можно использовать методы **ишеллфолдер** для перечисления содержимого вложенных папок, определения их свойств и т. д.

## <a name="determining-an-objects-parent-folder"></a>Определение родительской папки объекта

Если у вас есть объект ПИДЛ, может потребоваться обработчик для одного из интерфейсов, предоставляемых его родительской папкой. Например, если необходимо определить отображаемое имя, связанное с ПИДЛ с помощью [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), необходимо сначала получить интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) родительского объекта. Это можно сделать с помощью методик, описанных в предыдущих разделах. Однако гораздо более простой подход заключается в использовании функции Shell, [**шбиндтопарент**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent). Эта функция принимает полное ПИДЛ объекта и возвращает указанный указатель интерфейса в родительской папке. При необходимости он также возвращает одноуровневый ПИДЛ элемента для использования в таких методах, как [**ишеллфолдер:: жетаттрибутесоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).

В следующем примере консольное приложение получает ПИДЛ из специальной папки системы и возвращает ее отображаемое имя.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



Сначала приложение использует [**шжетфолдерлокатион**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) для получения Пидл системной папки. Затем он вызывает [**шбиндтопарент**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent), который возвращает указатель на интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) родительской папки и Пидл системной папки относительно ее родителя. Затем он использует метод [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) родительской папки для получения отображаемого имени системной папки. Поскольку **жетдисплайнамеоф** возвращает структуру [**стррет**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , [**стрреттобуф**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) используется для преобразования отображаемого имени в обычную строку. После отображения отображаемого имени указатели интерфейса освобождаются и система ПИДЛ освобождена. Обратите внимание, что не следует освобождать относительные ПИДЛ, возвращенные **шбиндтопарент**.

 

 
