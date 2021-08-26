---
description: Отладка компонентов, написанных на Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Отладка компонентов, написанных на Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0dc8e4d98a41f0059de8e3eb44deeb9dcd8e4fbfdc6dba0510bd227a189c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991184"
---
# <a name="debugging-components-written-in-visual-basic"></a>Отладка компонентов, написанных на Visual Basic

для отладки в определенных сценариях можно использовать среду разработки Microsoft Visual Basic 6,0. использование Visual Basic для отладки обеспечивает доступ к средствам, знакомым Visual Basic программистам. с другой стороны, поскольку во время отладки Visual Basic компоненты выполняются в процессе Visual Basic среды, может потребоваться отладка компонента после его компиляции с помощью среды разработки Microsoft Visual C++.

дополнительные сведения об отладке в Visual Basic интегрированной среде разработки (ide) см. [в разделе отладка в среде ide Visual Basic](debugging-in-the-visual-basic-ide.md). дополнительные сведения об отладке Visual Basic компонентов после их компиляции с помощью среды разработки Visual C++ см. в разделе [отладка, скомпилированная Visual Basic компонентов](debugging-compiled-visual-basic-components.md).

кроме того, некоторые ограничения, связанные с использованием среды Visual Basic для отладки компонентов с помощью MTS, были разрешены для COM+. дополнительные сведения см. в разделе [поддержка отладки COM+ Visual Basic, которая отличается от MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> если вы уже использовали Visual Basic на том же компьютере, что и COM+, возможно, вы заметили, что надстройка служб компонентов доступна в среде Visual Basic. Изначально в MTS эта функция была разработана для обновления реестра при каждой повторной компиляции компонента в приложении COM+. однако, учитывая характер взаимодействия реестра Microsoft Windows и базы данных регистрации COM+, некоторые параметры могут быть не обновлены полностью. Поэтому вместо использования команд, доступных в этой надстройке, следует удалить и переустановить компоненты, чтобы обновить параметры после повторной компиляции.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отладка компонентов, написанных на Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



