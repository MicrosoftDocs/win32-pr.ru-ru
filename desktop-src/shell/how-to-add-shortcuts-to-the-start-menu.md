---
description: Чтобы добавить элемент в подменю программы, выполните следующие действия.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Добавление ярлыков в меню "Пуск"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156475"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Добавление ярлыков в меню "Пуск"

Чтобы добавить элемент в подменю **программы** , выполните следующие действия.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Создайте [ссылку на оболочку](./links.md) с помощью интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .

### <a name="step-2"></a>Шаг 2.

Получите расположение папки Programs с помощью функции [**шжеткновнфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , передав [**\_ программы FOLDERID**](knownfolderid.md).

### <a name="step-3"></a>Шаг 3.

Добавьте ссылку оболочки в папку программы. Можно также создать папку в папке Programs и добавить ссылку в эту папку.

 

 
