---
description: В этом разделе описывается использование интерфейсов уровня страницы, обеспечивающих доступ к содержимому страницы в OM-модели XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Работа с интерфейсами страниц OM в XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693236"
---
# <a name="working-with-xps-om-page-interfaces"></a>Работа с интерфейсами страниц OM в XPS

В этом разделе описывается использование интерфейсов уровня страницы, обеспечивающих доступ к содержимому страницы в OM-модели XPS.



| Имя интерфейса                                                                                                                                                                              | Логические дочерние интерфейсы                                                                                                                                                                                            | Описание                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [**икспсомканвас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**икспсомглифс**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**икспсомпас**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | Корневой объект содержимого страницы.<br/> Этот объект представляет часть документа.<br/>                                                |
| [**икспсомшареабле**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [**икспсомвисуал**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [**икспсомматрикстрансформ**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [**икспсомжеометри**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [**икспсомбруш**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | Интерфейсы, производные от интерфейса [**икспсомшареабле**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) , могут храниться в словаре ресурсов и использоваться совместно.<br/> |
| [**икспсомремотедиктионариресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [**икспсомремотедиктионариресаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [**икспсомдиктионари**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | Содержит словарь ресурсов.<br/>                                                                                                         |
| [**икспсомдиктионари**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | Нет<br/>                                                                                                                                                                                                     | Ссылается на ресурсы, совместно используемые другими объектами.<br/>                                                                              |
| [**икспсомсторифрагментсресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | Нет<br/>                                                                                                                                                                                                     | Предоставляет доступ к содержимому потока ресурсов Сторифрагментс части документа.<br/>                                       |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Икспсомдиктионари**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[**икспсомдокументструктурересаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[**Интерфейс Икспсомпаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Интерфейс Икспсомремотедиктионариресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[**Интерфейс Икспсомремотедиктионариресаурцеколлектион**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[**Интерфейс Икспсомсторифрагментсресаурце**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




