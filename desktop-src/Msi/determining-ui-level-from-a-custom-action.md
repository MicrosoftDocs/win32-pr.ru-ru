---
description: Для пользовательского действия в таблице последовательности элементов пользовательского интерфейса или во внешнем исполняемом файле может потребоваться текущий уровень пользовательского интерфейса установки.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Определение уровня пользовательского интерфейса на основе настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998820"
---
# <a name="determining-ui-level-from-a-custom-action"></a><span data-ttu-id="c0078-103">Определение уровня пользовательского интерфейса на основе настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="c0078-103">Determining UI Level from a Custom Action</span></span>

<span data-ttu-id="c0078-104">Для пользовательского действия в таблице последовательности элементов пользовательского интерфейса или во внешнем исполняемом файле может потребоваться текущий уровень пользовательского интерфейса установки.</span><span class="sxs-lookup"><span data-stu-id="c0078-104">A custom action in a UI sequence table or an external executable file may need the current user interface level of the installation.</span></span> <span data-ttu-id="c0078-105">Например, пользовательское действие, имеющее диалоговое окно, должно отображать диалоговое окно только в том случае, если уровень пользовательского интерфейса является полным или ограниченным пользовательским интерфейсом, но не должен отображать диалоговое окно, если уровень пользовательского интерфейса — Basic UI или None.</span><span class="sxs-lookup"><span data-stu-id="c0078-105">For example, a custom action that has a dialog box should only display the dialog when the user interface level is Full UI or Reduced UI, it should not display the dialog if the user interface level is Basic UI or None.</span></span> <span data-ttu-id="c0078-106">Для определения текущего уровня пользовательского интерфейса следует использовать свойство [**duilevel**](uilevel.md) .</span><span class="sxs-lookup"><span data-stu-id="c0078-106">You should use the [**UILevel**](uilevel.md) property to determine the current user interface level.</span></span> <span data-ttu-id="c0078-107">Невозможно вызвать [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) из настраиваемого действия, и невозможно изменить свойство уровня пользовательского интерфейса из настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="c0078-107">You cannot call [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) from a custom action and it is not possible to change the UI level property from within a custom action.</span></span>

<span data-ttu-id="c0078-108">Рекомендуется, чтобы настраиваемые действия не использовали уровень пользовательского интерфейса в качестве условия для отправки сообщений об ошибках в установщик, так как это может помешать работе с ведением журнала и внешними сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c0078-108">It is recommended that custom actions not use the UI level as a condition for sending error messages to the installer because this can interfere with logging and external messages.</span></span>

 

 



