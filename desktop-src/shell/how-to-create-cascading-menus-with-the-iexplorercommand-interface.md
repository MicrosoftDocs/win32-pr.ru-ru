---
description: 'Другим вариантом добавления команд в каскадное меню является Иексплореркомманд:: Енумсубкоммандс.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Создание каскадных меню с помощью интерфейса Иексплореркомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436099"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Создание каскадных меню с помощью интерфейса Иексплореркомманд

Другим вариантом добавления команд в каскадное меню является [**иексплореркомманд:: енумсубкоммандс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Этот метод позволяет источникам данных, которые предоставляют команды командного модуля через интерфейс [**иексплореркоммандпровидер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) , использовать эти команды в качестве команд в контекстном меню. в Windows 7 и более поздних версиях вы можете предоставить ту же реализацию команды с помощью интерфейса [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , как и при использовании интерфейса [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .

## <a name="instructions"></a>Инструкции


Следующие два снимка экрана иллюстрируют использование каскадных меню в папке **Devices** .

![Снимок экрана, на котором показан пример каскадного меню в папке Devices.](images/file-assoc/FileCascadeMenu.png)

![снимок экрана, показывающий пример каскадного меню в папке "устройства"](images/file-assoc/cascadeDevices2.png)

## <a name="remarks"></a>Remarks

> [!Note]  
> Так как [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) поддерживает только внутрипроцессный активацию, рекомендуется использовать их в качестве источников данных оболочки, которые должны совместно использовать реализацию команд и контекстных меню.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**иексплореркоммандпровидер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
