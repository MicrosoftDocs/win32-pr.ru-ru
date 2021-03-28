---
description: С помощью реестра можно указать, что при просмотре точки соединения будет открываться корневое представление, а не представление содержимого соответствующего расширения по умолчанию.
title: Открытие корневого представления точки соединения в реестре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264416"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="71af5-103">Открытие корневого представления точки соединения в реестре</span><span class="sxs-lookup"><span data-stu-id="71af5-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="71af5-104">С помощью реестра можно указать, что при просмотре точки соединения будет открываться корневое представление, а не представление содержимого соответствующего расширения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71af5-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="71af5-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="71af5-105">Instructions</span></span>


<span data-ttu-id="71af5-106">Чтобы указать, что при просмотре точки соединения необходимо открыть корневое представление, добавьте  \\ **команду** Open и **Изучите** \\ подразделы **команды** в подразделе **CLSID** расширения, используя значения по умолчанию, назначенные командным строкам, приведенным ниже:</span><span class="sxs-lookup"><span data-stu-id="71af5-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

<span data-ttu-id="71af5-107">После добавления этих значений запускается экземпляр Explorer.exe для отображения содержимого расширения в виде корневого представления, когда пользователь выбирает точку соединения.</span><span class="sxs-lookup"><span data-stu-id="71af5-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71af5-108">См. также</span><span class="sxs-lookup"><span data-stu-id="71af5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71af5-109">Указание расположения расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="71af5-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="71af5-110">Открытие корневого представления точки соединения через файл ярлыка</span><span class="sxs-lookup"><span data-stu-id="71af5-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



