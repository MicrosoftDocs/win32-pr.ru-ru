---
description: Для создания простого пользовательского интерфейса разработчики пакетов установки могут использовать структуру пользовательского интерфейса, которая соответствует поведению мастера интерфейса.
ms.assetid: c69ba452-3c2e-47d7-8ea0-8f8f9e6b58c8
title: Поведение мастера пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045aa59fe510ff10f428d0a7c74549ce4d817157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818544"
---
# <a name="user-interface-wizard-behavior"></a><span data-ttu-id="51fde-103">Поведение мастера пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="51fde-103">User Interface Wizard Behavior</span></span>

<span data-ttu-id="51fde-104">Для создания простого пользовательского интерфейса разработчики пакетов установки могут использовать структуру пользовательского интерфейса, которая соответствует поведению мастера интерфейса.</span><span class="sxs-lookup"><span data-stu-id="51fde-104">To author a simple user interface, developers of installation packages can utilize a user interface design that adheres to interface wizard behavior.</span></span>

<span data-ttu-id="51fde-105">Поведение мастера термина "Пользовательский интерфейс" означает, что каждое диалоговое окно в последовательности содержит **следующую>>** кнопку, которую пользователь нажимает для перехода к следующему диалоговому окну после ввода данных или настройки сведений в текущем диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="51fde-105">The term user interface wizard behavior means that each dialog box in a sequence contains a **Next>>** button, which the user clicks to move to the next dialog box after entering data or configuring information in the current dialog box.</span></span> <span data-ttu-id="51fde-106">Если пользователь решает вернуться и изменить любые сведения, указанные в предыдущем диалоговом окне, каждое диалоговое окно содержит кнопку **<<назад** , которую пользователь щелкает для возврата.</span><span class="sxs-lookup"><span data-stu-id="51fde-106">If the user decides to go back and change any information entered in a previous dialog box, each dialog box contains a **<<Previous** button that the user clicks to go back.</span></span> <span data-ttu-id="51fde-107">В конце последовательности мастера пользователь нажимает кнопку **Готово** , чтобы начать процесс установки.</span><span class="sxs-lookup"><span data-stu-id="51fde-107">At the end of the wizard sequence, the user clicks a **Finish** button to begin the installation process.</span></span>

<span data-ttu-id="51fde-108">Пользовательский интерфейс, описанный в примере ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, соответствует поведению мастера пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="51fde-108">The UI described in the UI example adheres to user interface wizard behavior.</span></span> <span data-ttu-id="51fde-109">См. [Пример установки](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="51fde-109">See [An Installation Example](an-installation-example.md).</span></span>

 

 



