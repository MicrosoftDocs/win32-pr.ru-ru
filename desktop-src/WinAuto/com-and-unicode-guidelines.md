---
title: Рекомендации по COM и Юникод
description: Поскольку Microsoft Active Accessibility основан на модели COM, разработчикам нужен умеренный уровень понимания COM-объектов и интерфейсов и должен знать, как выполнять основные задачи (например, как инициализировать библиотеку COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710301"
---
# <a name="com-and-unicode-guidelines"></a>Рекомендации по COM и Юникод

Поскольку Microsoft Active Accessibility основан на модели COM, разработчикам нужен умеренный уровень понимания COM-объектов и интерфейсов и должен знать, как выполнять основные задачи (например, как инициализировать библиотеку COM). Разработчикам серверов необходимо понимать, как проектировать классы, реализующие интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , и как создавать объекты со специальными возможностями.

Также необходим средний уровень понимания Юникода, чтобы использовать многие функции Microsoft Active Accessibility, возвращающие строки.

Чтобы эффективно использовать Microsoft Active Accessibility, необходимо понимать следующие функции COM и Юникода, структуры, типы данных и интерфейсы. Ограниченные сведения о некоторых из этих элементов приведены в этой документации.

### <a name="functions"></a>Функции

-   [**олеинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**Вариантинит**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) и [ **вариантклеар**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) и [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**Сисаллокстринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) и [ **сисфристринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Структуры и типы данных:

-   [**ЗНАЧЕНИЕ**](variant-structure.md)
-   [**СОСТАВ**](/windows/desktop/com/structure-of-com-error-codes)
-   [**ОСВОБОЖДАЕМОЙ**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>COM-интерфейсы:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>Содержание раздела

-   [Структура варианта](variant-structure.md)
-   [Интерфейс IDispatch](idispatch-interface.md)
-   [Преобразование строк Юникода и ANSI](converting-unicode-and-ansi-strings.md)

 

 