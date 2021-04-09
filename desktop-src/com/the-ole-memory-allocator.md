---
title: Распределитель памяти OLE
description: Распределитель памяти OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134631"
---
# <a name="the-ole-memory-allocator"></a>Распределитель памяти OLE

Библиотека COM предоставляет реализацию механизма выделения памяти, который является потокобезопасным. (То есть это не может вызвать проблемы в многопоточных ситуациях.) Всякий раз, когда владение выделенным блоком памяти передается через COM-интерфейс или между клиентом и библиотекой COM, необходимо использовать этот распределитель COM для выделения памяти. Внутреннее выделение объекта может использовать любую схему распределения, но распределитель памяти COM — это удобный, эффективный и потокобезопасный распределитель.

Вызов функции API [**кожетмаллок**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) предоставляет указатель на распределитель OLE, который является реализацией [**интерфейса выделения**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) . Однако более эффективно вызывать вспомогательные функции [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**котаскмемреаллок**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)и [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), которые заключают указатель на распределитель памяти задачи, вызывая **соответствующий метод выделения** , а затем освобождая указатель на распределитель.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление выделением памяти](managing-memory-allocation.md)
</dt> <dt>

[Библиотека COM](the-com-library.md)
</dt> </dl>

 

 