---
description: Установщик Windows предоставляет множество встроенных действий для выполнения процесса установки. Список этих действий см. в справочнике по стандартным действиям.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Особые действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080924"
---
# <a name="custom-actions"></a><span data-ttu-id="f7b26-104">Особые действия</span><span class="sxs-lookup"><span data-stu-id="f7b26-104">Custom Actions</span></span>

<span data-ttu-id="f7b26-105">Установщик Windows предоставляет множество встроенных действий для выполнения процесса установки.</span><span class="sxs-lookup"><span data-stu-id="f7b26-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="f7b26-106">Список этих действий см. в [справочнике по стандартным действиям](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f7b26-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="f7b26-107">Стандартные действия достаточно для выполнения установки в большинстве случаев.</span><span class="sxs-lookup"><span data-stu-id="f7b26-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="f7b26-108">Однако существуют ситуации, когда разработчик пакета установки находит необходимость в написании настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="f7b26-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="f7b26-109">Пример:</span><span class="sxs-lookup"><span data-stu-id="f7b26-109">For example:</span></span>

-   <span data-ttu-id="f7b26-110">Необходимо запустить исполняемый файл во время установки, который устанавливается на компьютере пользователя или устанавливается вместе с приложением.</span><span class="sxs-lookup"><span data-stu-id="f7b26-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="f7b26-111">Необходимо вызывать специальные функции во время установки, определенные в библиотеке динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="f7b26-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="f7b26-112">Вы хотите использовать функции, написанные на языках разработки Microsoft Visual Basic Scripting Edition или в тексте литерального скрипта Microsoft JScript во время установки.</span><span class="sxs-lookup"><span data-stu-id="f7b26-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="f7b26-113">Необходимо отложить выполнение некоторых действий до момента выполнения скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="f7b26-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="f7b26-114">Необходимо добавить сведения о времени и ходе выполнения в элемент управления ProgressBar и элемент управления Text TimeRemaining.</span><span class="sxs-lookup"><span data-stu-id="f7b26-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="f7b26-115">В следующих разделах описываются пользовательские действия и способы их включения в пакет установки.</span><span class="sxs-lookup"><span data-stu-id="f7b26-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="f7b26-116">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="f7b26-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="f7b26-117">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="f7b26-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="f7b26-118">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="f7b26-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="f7b26-119">Сводный список всех типов настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="f7b26-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 



