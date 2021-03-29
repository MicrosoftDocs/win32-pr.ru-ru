---
title: Маршалирование типов данных OLE
description: Маршалирование автоматизации и типов данных OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL и COM MIDL, маршалирование типов данных OLE
- Маршалирование MIDL
- OLE Data MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790015"
---
# <a name="marshaling-ole-data-types"></a>Маршалирование типов данных OLE

Чтобы упростить использование определенных типов данных автоматизации и OLE, а также некоторых системных дескрипторов, часто используемых в COM, typedef для этих типов данных и связанные с ними вспомогательные функции доступны путем импорта файлов IDL Windows и связывания с DLL-файлами OLE и Automation. Эти файлы автоматически устанавливаются в системе.

-   Чтобы использовать тип данных [**BSTR**](/previous-versions/windows/desktop/automat/bstr) в удаленных вызовах процедур, импортируйте файл втипес. idl в файл определения интерфейса (IDL) и свяжите с oleaut32. lib при создании распределенного приложения. Это позволит вашим заглушкам использовать готовые вспомогательные функции **BSTR \_ усерсизе**, **BSTR \_ Усермаршал**, **BSTR \_ усерунмаршал** и **BSTR \_ усерфри**.
-   Чтобы использовать другие типы данных автоматизации, такие как [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) и [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray), или типы, использующие эти типы (например, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) и [**ексцепинфо**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), импортируйте файл обжидл. idl в IDL-файл и свяжите его с oleaut32. lib во время сборки. Это позволит использовать соответствующие вспомогательные подпрограммы.
-   Чтобы использовать типы данных OLE (такие как КЛИПФОРМАТ, СНБ, СТГМЕДИУМ, ASYNC \_ стгмедиум) или системные дескрипторы (например, хметафиле \_ PICT, ХЕНХМЕТАФИЛЕ, ХМЕТАФИЛЕ, ХБИТМАП, ХПАЛЕТТЕ и hglobal), импортируйте файл objidl. idl в файл определения интерфейса и свяжите его со сборкой ole32. lib во время сборки.
-   Следующие дескрипторы OLE также определяются с помощью атрибута **\[ Wire- \_ Marshal \]** , но только в качестве дескрипторов на компьютере, так как они не могут использоваться в удаленных вызовах процедур на других компьютерах в настоящее время: HWND, HMENU, хакцел, HDC, хфонт, Хикон, хбруш. Импортируйте файл обжидл. idl в IDL-файл и свяжите с ole32. lib во время сборки, чтобы использовать эти дескрипторы в процессе межпроцессного взаимодействия на одном компьютере.

Дополнительные сведения см. [в разделе атрибут проводного \_ маршалирования](/windows/desktop/Rpc/the-wire-marshal-attribute), [тип \_ усерсизе](/windows/desktop/Rpc/the-type-usersize-function), функция типа [ \_ усермаршал](/windows/desktop/Rpc/the-type-usermarshal-function), функция типа [ \_ Усерунмаршал](/windows/desktop/Rpc/the-type-userunmarshal-function), функция [Type \_ усерфри](/windows/desktop/Rpc/the-type-userfree-function)и [целевые заглушки для конкретных 32-разрядных или 64-разрядных платформ](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 