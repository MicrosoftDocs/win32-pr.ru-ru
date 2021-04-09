---
title: Вспомогательные функции для создания экземпляра
description: Вспомогательные функции для создания экземпляра
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070667"
---
# <a name="instance-creation-helper-functions"></a>Вспомогательные функции для создания экземпляра

В предыдущих выпусках COM основным механизмом, используемым для создания экземпляра объекта, была функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Эта функция инкапсулирует процесс создания объекта класса, используя его для создания нового экземпляра и освобождения объекта класса. Другой функцией этого типа является более конкретный [**олекреате**](/windows/desktop/api/ole/nf-ole-olecreate), вспомогательный метод составного документа OLE, который создает объект класса и получает указатель на запрошенный объект.

Чтобы сгладить процесс создания экземпляров в распределенных системах, в модели COM появились четыре важных новых механизма создания экземпляров:

-   Моникеры класса и [ **иклассактиватор**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Моникер класса позволяет определить класс объекта и обычно используется с другим моникером, например моникером файла, для указания расположения объекта. Это позволяет выполнить привязку к объекту и указать сервер, который должен быть запущен для этого объекта. Моникеры класса также могут состоять из имен справа от моникеров, поддерживающих привязку к интерфейсу [**иклассактиватор**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Дополнительные сведения см. в разделе [моникеры класса](class-monikers.md).

[**Кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) расширяет [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы можно было создать один неинициализированный объект, связанный с данным идентификатором CLSID, на указанном удаленном компьютере. Кроме того, вместо того, чтобы запрашивать один интерфейс и получать один указатель на этот интерфейс, **кокреатеинстанцеекс** делает возможным запрос нескольких интерфейсов и (при наличии) получать указатели на них в одном цикле приема-передачи, тем самым разрешая меньшее количество обращений между компьютерами. Это может сделать взаимодействие удаленного объекта гораздо более эффективным. Для этого в функции используется массив структур с [**несколькими \_ qiми**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) .

Для создания объекта через [**кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) все равно требуется инициализировать объект с помощью вызова одного из интерфейсов инициализации (например, [**Иперсистстораже:: Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)). Вспомогательные функции [**кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) и [**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) инкапсулируют возможности создания экземпляров **кокреатеинстанцеекс** и инициализации, первый из файлов и второй из хранилища.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание объекта через объект класса](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 