---
description: Отладка компонентов, написанных на Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Отладка компонентов, написанных на Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701281"
---
# <a name="debugging-components-written-in-visual-basic"></a>Отладка компонентов, написанных на Visual Basic

Для отладки в определенных сценариях можно использовать среду разработки Microsoft Visual Basic 6,0. Использование Visual Basic для отладки обеспечивает доступ к средствам, знакомым Visual Basic программистам. С другой стороны, поскольку во время отладки Visual Basic компоненты выполняются в процессе Visual Basic среды, может потребоваться отладка компонента после его компиляции с помощью среды разработки Microsoft Visual C++.

Дополнительные сведения об отладке в Visual Basic интегрированной среде разработки (IDE) см. [в разделе Отладка в среде ide Visual Basic](debugging-in-the-visual-basic-ide.md). Дополнительные сведения об отладке Visual Basic компонентов после их компиляции с помощью среды разработки Visual C++ см. в разделе [Отладка, скомпилированная Visual Basic компонентов](debugging-compiled-visual-basic-components.md).

Кроме того, некоторые ограничения, связанные с использованием среды Visual Basic для отладки компонентов с помощью MTS, были разрешены для COM+. Дополнительные сведения см. в разделе [Поддержка отладки COM+ Visual Basic, которая отличается от MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> Если вы уже использовали Visual Basic на том же компьютере, что и COM+, возможно, вы заметили, что надстройка служб компонентов доступна в среде Visual Basic. Изначально в MTS эта функция была разработана для обновления реестра при каждой повторной компиляции компонента в приложении COM+. Однако, учитывая характер взаимодействия реестра Microsoft Windows и базы данных регистрации COM+, некоторые параметры могут быть не обновлены полностью. Поэтому вместо использования команд, доступных в этой надстройке, следует удалить и переустановить компоненты, чтобы обновить параметры после повторной компиляции.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отладка компонентов, написанных на Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



