---
description: Описание процедуры чтения существующего документа XPS из файла в объектную модель XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Чтение XPS-документа в объектную модель XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348222"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Чтение XPS-документа в объектную модель XPS

Описание процедуры чтения существующего документа XPS из файла в объектную модель XPS.

Чтобы создать объект XPS из документа XPS, вызовите метод [**икспсомобжектфактори:: креатепаккажефромфиле**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .

Прежде чем использовать эти примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Пример кода

В следующем примере кода предполагается, что инициализация, описанная в разделе [Инициализация OM-модели XPS](xps-object-model-initialization.md) , выполнена успешно.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Чтобы создать объект XPS из документа XPS, хранящегося в виде потока, вызовите [**икспсомобжектфактори:: креатепаккажефромстреам**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).

## <a name="remarks"></a>Комментарии

Если вы написали модуль XPS сразу же после считывания пакета XPS в него, часть исходного содержимого может быть утеряна или изменена.

Некоторые изменения, которые могут возникнуть в этом случае, перечислены в следующей таблице:

| Функция документа                      | Действие                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Цифровые подписи<br/>         | Удалено из документа<br/>                               |
| Часть Дискардконтрол<br/>        | Удалено из документа<br/>                               |
| Части внешнего документа<br/>     | Удалено из документа<br/>                               |
| Разметка FixedPage<br/>           | Изменено с исходного<br/>                              |
| Разметка словаря ресурсов<br/> | Изменено с исходного, если установлен флаг оптимизации<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Навигация по OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Запись текста в объектную модель XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Рисование графики в OM-объекте XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Размещение изображений в объектной модели XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Используется в этом разделе**
</dt> <dt>

[**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Инициализация объектной модели XPS](xps-object-model-initialization.md)
</dt> <dt>

[API для упаковки](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Справочник по API документов XPS](xps-programming-reference.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

