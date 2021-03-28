---
description: 'Другим вариантом добавления команд в каскадное меню является Иексплореркомманд:: Енумсубкоммандс.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Создание каскадных меню с помощью интерфейса Иексплореркомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559954"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Создание каскадных меню с помощью интерфейса Иексплореркомманд

Другим вариантом добавления команд в каскадное меню является [**иексплореркомманд:: енумсубкоммандс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Этот метод позволяет источникам данных, которые предоставляют команды командного модуля через интерфейс [**иексплореркоммандпровидер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) , использовать эти команды в качестве команд в контекстном меню. В Windows 7 и более поздних версиях вы можете предоставить ту же реализацию команды с помощью интерфейса [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , как и с помощью интерфейса [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .

## <a name="instructions"></a>Инструкции


Следующие два снимка экрана иллюстрируют использование каскадных меню в папке **Devices** .

![Снимок экрана, на котором показан пример каскадного меню в папке Devices.](images/file-assoc/filecascademenu.png)

![снимок экрана, показывающий пример каскадного меню в папке "устройства"](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a>Примечания

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

 

 
