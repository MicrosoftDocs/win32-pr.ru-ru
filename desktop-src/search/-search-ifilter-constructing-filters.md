---
description: Важно понимать необходимую структуру DLL обработчика фильтров (реализацию интерфейса IFilter).
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: реализация обработчиков фильтров в Windowsном поиске
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b1c55f0cfc50b75a6e206e2479ff6849d102a42a35b75026f8b6d3f37766b41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680883"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>реализация обработчиков фильтров в Windowsном поиске

Важно понимать необходимую структуру DLL обработчика фильтров (реализацию интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

Этот раздел организован следующим образом:

- [Реализация и экспорт точек входа библиотеки DLL](#implementing-and-exporting-the-dll-entry-points)
- [Реализация класса IFilter и фабрики классов](#implementing-the-ifilter-class-and-class-factory)
- [Наследование COM-интерфейсов](#inheriting-the-com-interfaces)
- [Реализация методов COM-интерфейса](#implementing-the-com-interface-methods)
  - [Нереализованные методы COM](#com-methods-that-are-not-implemented)
- [Дополнительные ресурсы](#additional-resources)
- [Связанные темы](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>Реализация и экспорт точек входа библиотеки DLL

Каждая библиотека DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) (обозначенная Ifilter.dll в этом разделе) должна реализовывать и экспортировать следующие точки входа. Эти точки входа обычно экспортируются с помощью файла определения модуля (DEF) для интерфейса **IFilter** или с помощью ключевого слова **\_ \_ declspec (dllexport)** . DLL-файл может быть зарегистрирован в любой папке, но обычно находится в папке% SystemRoot% \\ System32.

Точки входа библиотеки DLL перечислены и описаны в следующей таблице.

| Имя DLL                                                                                     | Описание библиотеки DLL                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Регистрация](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | Точка входа [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) регистрирует библиотеку DLL в качестве фильтра в реестре. Вы регистрируете библиотеку DLL, запустив программу regsvr32.exe с именем DLL-файла интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) в качестве аргумента: `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [Функция DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | Точка входа [функции DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) удаляет библиотеку DLL в качестве постоянного обработчика в реестре. Отмените регистрацию библиотеки DLL, запустив программу regsvr32.exe с `/u` флагом: `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [Функция DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | Клиент индексирования содержимого вызывает точку входа [функции DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) с помощью модели COM, чтобы создать объект фабрики класса для интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и получить указатель на интерфейс фабрики класса этого объекта.                                               |
| [Функция DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | Клиент индексирования содержимого вызывает точку входа [функции DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) через COM, чтобы определить, возможно ли выгрузить DLL-библиотеку [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  . Интерфейс **IFilter** выгружается после того, как он не используется в течение интервала времени, как указано в значении реестра филтеридлетимеаут. |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>Реализация класса IFilter и фабрики классов

По крайней мере два класса, такие как Кфилтер и Кфилтеркф, обычно реализуются каждой DLL-библиотекой [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Класс Кфилтер создает объект интерфейса **IFilter** , реализующий функцию фильтрации содержимого. Его функции члена реализуют методы интерфейса интерфейса **IFilter** . Каждый класс **IFilter** требует уникального идентификатора класса (CLSID), создаваемого реализацией интерфейса **IFilter** .

Класс Кфилтеркф создает объект фабрики класса для интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Фабрика класса вызывается через интерфейс [интерфейса IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) в точке входа [функции DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) библиотеки DLL. Класс Кфилтеркф создает объект Кфилтер и возвращает указатель на [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown). В более сложных случаях **IFilter** может реализовать иерархию классов вместо одного класса кфилтер.

## <a name="inheriting-the-com-interfaces"></a>Наследование COM-интерфейсов

Windows В поиске 3,0 и более поздних версиях необходимо использовать [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) по следующим причинам:

- Для обеспечения производительности и будущей совместимости.
- Для повышения безопасности. IFilter, реализованные с помощью [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) , более безопасны, так как контекст, в котором выполняется интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , не требует наличия прав на открытие файлов на диске или по сети.
- хотя Windows поиск использует только [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), класс интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) также может наследовать реализации интерфейса [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) и (или) интерфейсов [иперсистстораже](/windows/win32/api/objidl/nn-objidl-ipersiststorage) для обратной совместимости.

Эти интерфейсы объявляются в файлах, включаемых из \\ каталога мссдк include, и имеют предварительно определенные идентификаторы интерфейса (идентификаторов IID). Клиент индексирования содержимого запрашивает интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) через [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , чтобы определить, какой из этих интерфейсов следует использовать при фильтрации содержимого.

## <a name="implementing-the-com-interface-methods"></a>Реализация методов COM-интерфейса

Интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) реализует методы [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) как для класса интерфейса **IFilter** , так и для фабрики класса интерфейса **IFilter** . В следующей таблице перечислены интерфейсы и методы интерфейса **IFilter** , которые должны реализовываться **интерфейсом IFilter,** в порядке vtable. Интерфейс **IFilter** должен реализовывать не менее [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), но может реализовывать дополнительные интерфейсы, производные от IPersist.

| Интерфейс COM                                                                             | Метод                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Интерфейс IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | CreateInstance, Локксервер                                                                                                                                                                                                                                                     |
| [Интерфейс IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | ЖетлиЦинфо, Рекуестликкэй, Креатеинстанцелик                                                                                                                                                                                                                                   |
| [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init), [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)GetText, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext), [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue), [**IFilter:: биндрегион**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [Интерфейс IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [Интерфейс IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty, Load, Save, Савекомплетед, Жеткурфиле                                                                                                                                                                                                                                 |
| [Интерфейс Иперсистстораже](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty, Load, Save, Жетсиземакс                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty, Load, Save, Жетсиземакс                                                                                                                                                                                                                                                |

На странице ссылки для каждого метода указаны параметры и поведение для этого метода. Каждая эталонная страница также предоставляет коды результатов для реализации этого метода. Справочные страницы для методов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) предоставляют коды, зависящие от интерфейса, [в \_ итфах](../com/codes-in-facility-itf.md) результатов, которые должны быть реализованы, а клиент индексирования содержимого также может обрабатывать любые общие коды результатов, такие как устройства \_ null и устройства \_ Win32. Дополнительные сведения см. в разделе [структура кодов ошибок COM](../com/structure-of-com-error-codes.md).

### <a name="com-methods-that-are-not-implemented"></a>Нереализованные методы COM

Интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) должен реализовывать по меньшей мере [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), но не должен реализовывать дополнительные интерфейсы, производные от IPersist.

Windows Поиск не требует реализации методов COM, перечисленных в следующей таблице.

| Необязательный метод                               | Описание                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream:: IsDirty                                   | Фильтры должны возвращать E \_ нотимпл. |
| IPersistStream:: Save                                      | Фильтры должны возвращать E \_ нотимпл. |
| IPersistStream:: Жетсиземакс                                | Фильтры должны возвращать E \_ нотимпл. |
| [**IFilter:: Биндрегион**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Фильтры должны возвращать E \_ нотимпл. |

## <a name="additional-resources"></a>Дополнительные ресурсы

- пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).
- Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).
- Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Связанные темы

[Разработка обработчиков фильтров](-search-ifilter-conceptual.md)

[основные сведения о обработчиках фильтров в Windows поиске](-search-ifilter-about.md)

[рекомендации по созданию обработчиков фильтров в Windowsном поиске](-search-3x-wds-extidx-filters.md)

[Возвращение свойств из обработчика фильтра](-search-ifilter-property-filtering.md)

[Обработчики фильтров, поставляемые с Windows](-search-ifilter-implementations.md)

[Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md)

[Тестирование обработчиков фильтров](-search-ifilter-testing-filters.md)
